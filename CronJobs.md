# CronJobs

**This plugin is for Vietnamese servers only. Do not resell, share, reup this plugin without my permission**

**Plugin này chỉ dành cho máy chủ VN. Nghiêm cấm bán lại, chia sẻ, đăng tải lại plugin này mà chưa có sự cho phép của mình**

**Official download link/Linh tải chính thức:** https://minecraftvn.net/t22146 

### I. HƯỠNG DẪN
1/ Thực hiện lệnh ngay khi plugin đã bật
- VD 1: chạy ngay lệnh /this is a command
```~ this is a command```

2/ Sau một khoảng thời gian từ khi plugin bật mới thực hiện lệnh
- VD 1 : chạy lệnh /this is a command sau 10 giây<br>
```@wait:10s ~ this is a command```
- VD 2 : chạy lệnh /this is a command sau 1 phút 30 giây<br>
```@wait:1m,30s ~ this is a command```
- VD 3 : chạy lệnh /this is a command sau 3 tiếng rưỡi<br>
```@wait:3h,30m ~ this is a command```

3/ Thực hiện lệnh ngay khi plugin đã bật, lặp lại sau một khoảng thời gian
- VD 1: chạy lệnh /this is a command mỗi một tiếng<br>
```@repeat:1h ~ this is a command```

4/ Sau một khoảng thời gian từ khi plugin bật mới thực hiện lệnh, rồi lặp lại sau một khoảng thời gian
- VD 1: Đợi 5 phút rồi chạy lệnh /this is a command, rồi cứ mỗi hai tiếng là lặp lại lệnh đó<br>
```@wait:5m @repeat:2h ~ this is a command```

5/ Thực hiện lệnh ngay khi plugin đã bật, lặp lại sau một khoảng thời gian cho đến khi đạt đủ số lần
- VD 1: Chạy lệnh /this is a command mỗi một tiếng cho đến khi đủ 10 lần<br>
```@repeat:1h @to:repeat(10) ~ this is a command```
- VD 2: Chạy lệnh /this is a command mỗi ba tiếng cho đến khi đủ 20 lần<br>
```@repeat:3d @to:repeat(20) ~ this is a command```

6/ Sau một khoảng thời gian từ khi plugin bật mới thực hiện lệnh, rồi lặp lại sau một khoảng thời gian đến khi đạt đủ số lần
- VD 1: Chờ 5 ngày, rồi lặp lại lệnh /this is a command mỗi ba tuần cho đến khi đủ 20 lần<br>
```@wait:5d @repeat:3w @to:repeat(20) ~ this is a command```

7/ Thực hiện lệnh lặp đi lặp lại đến khi chạm mốc thời gian/khoảng thời gian
- VD 1: Lặp lại lệnh /this is a command mỗi một giờ cho đến khi đủ năm tuần thì dừng<br>
```@repeat:1h @to:duration(5w) ~ this is a command```
- VD 2: lặp lại lệnh /this is a command mỗi một tuần cho đến ngày 31/12/2020 thì dừng<br>
```@repeat:1w @to:date(2020y,12m,31d) ~ this is a command```

8/ Thực hiện lệnh sau khi đã vượt qua mốc thời gian
- VD 1: Tới ngày 10/12/2019 (hoặc hơn) thì chạy lệnh /this is a command một lần duy nhất<br>
```@from:2019y,12m,10d ~ this is a command```
- VD 2: Kể từ ngày 10/12/2019 đến ngày 10/3/2020, cứ mỗi hai tuần sẽ chạy lệnh /this is a command một lần<br>
```@from:2019y,12m,10d @repeat:2w @to:date(2020y,3m,10d) ~ this is a command```

9/ Chạy lệnh bằng luồng ngoài
- VD 1: Chờ 20 giây rồi chạy lệnh /this is a command bằng luồng ngoài<br>
```@wait:20s @async ~ this is a command```

10/ Ghi chú
Thêm dấu # ở trước mỗi dòng<br>
```#đây là ghi chú```<br>
_Chú ý, dấu # phải đặt ở ngay đầu, nếu ở vị trí khác thì vẫn tính là lệnh_

### II. THAM SỐ
- @async: yêu cầu lệnh chạy bằng luồng ngoài (tác vụ không đồng bộ). Chú ý là tham số này còn tùy thuộc vào lệnh, không phải lệnh nào cũng dùng được.
- @from: là mốc thời gian bắt đầu **định dạng: mốc thời gian**<br>
VD 1: ```@from:2019y,5M,36d```<br>
VD 2: ```@from:2019y,5M,36d,15h,28m,40s```
- @wait: là thời gian chờ **định dạng: khoảng thời gian**<br>
VD 1: ```@wait:10s```<br>
VD 2: ```@wait:3w,4y```
- @repeat: là thời gian lặp lại **định dạng: khoảng thời gian**<br>
VD 1: ```@repeat:1d```<br>
VD 2: ```@repeat:10s```
- @to:repeat(_<SỐ LẦN>_) là thời gian kết thúc **định dạng: số lần lặp lại**<br>
VD 1: ```@to:repeat(99)```
- @to:duration(_<KHOẢNG THỜI GIAN>_) là thời gian kết thúc **định dạng: khoảng thời gian**<br>
VD 1: ```@to:duration(1t)```
- @to:date là thời gian kết thúc **định dạng: mốc thời gian**<br>
VD 1: ```@to:date(2020y,3M,10d)```

**(!) CHÚ Ý:**
- @from không thể dùng với @wait
- @to chỉ có thể dùng khi có @repeat
- Với mốc thời gian, bạn có thể thêm dấu phẩy để ngăn cách các đơn vị thời gian. Các đơn vị thời gian có thể dùng: phút(m), giờ(h), giây(s), ngày(d), tháng(M), năm(y). Trong đó ngày, tháng, năm là bắt buộc.
- Khoảng thời gian: phút(m), giờ(h), giây(s), ngày(d), tháng 30 ngày(M hoặc M30), năm(y), tuần(w), tháng 31 ngày(M31), tháng 29 ngày(M29), tháng 28 ngày(M28), năm nhuần(ly), tick(t), milisecond(ms)

### III. VÍ DỤ KHÁC
```
~ bc &aMAY CHU DA BAT!
@wait:5m @async ~ bc &aMAY CHU DA BAT!
@wait:30m @repeat:5w ~ bc &aMAY CHU DA BAT!
@repeat:1m @to:repeat(50) ~ bc DANG CO EVENT ABCXYZ. MOI MOI NGHUOI THAM GIA!!!
@repeat:1h @to:duration(10w) ~ abc SPAM CHAT !@$%^&
@repeat:1h @to:date(2018y,5M,36d) ~ abc SPAM CHAT !@$%^&
@from:2018y,5M,36d @repeat:3d @to:repeat(15) ~ bc TICH CUC QUAY TAY VAN MAY SE DEN
@from:2018y,5M,36d @repeat:3d,1m @to:repeat(15),date(2018y,5M,36d) ~ killall
```

### IV. LỆNH BỔ SUNG
Plugin có bổ sung vài lệnh phòng trường hợp máy chủ của bạn thiếu plugin, các lệnh đó gồm:
- /cj bc <tin nhắn>: phát ra tin nhắn cho toàn máy chủ **CHÚ Ý KHÔNG @ASYNC**
- /cj fc <người chơi> <lệnh>: bắt người chơi chạy lệnh **CHÚ Ý KHÔNG @ASYNC**
- /cj fca <lệnh>: bắt mọi người chơi chạy lệnh **CHÚ Ý KHÔNG @ASYNC**

(*) Các lệnh trên đều yêu cầu quyền cronjobs.admin
