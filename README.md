# aap
anhcraft's archived plugins

## HopQua
- Công dụng: tạo ra hộp quà
- Yêu cầu: SpaciousLib
- Hưỡng dẫn:
  + Cầm bất kỳ vật phẩm muốn tạo thành hộp quà, gõ /hopqua
  + Chuột phải để mở menu, đưa các vật phẩm mong muốn vào
  + Shift + Chuột phải để tạo hộp quà hoàn chỉnh
  + Hộp quà hoàn chỉnh có thể mở bằng cách chuột phải
- Quyền hạn:
  + hopqua.admin (để tạo hộp quà)
  + hopqua.use (để dùng hộp quà)
  
## ImportExportItems
- Công dụng: nhập, xuất vật phẩm
- Lệnh:
  + /imi: nhập vật phẩm với tên XXX và trao cho bản thân
  + /imif: nhập vật phẩm với tên XXX và trao cho người khác
  + /imai: nhập mọi vật phẩm đã lưu
  + /exi: xuất vật phẩm với tên XXX
- Quyền hạn:
  + importexportitems.import (cho /imi)
  + importexportitems.importfor (cho /imif)
  + importexportitems.importall (cho /imai)
  + importexportitems.export (cho /exi)
  
## MyThicsMobGenerator
- Công dụng: tạo boss, item, skill MyThics bằng GUI
- Yêu cầu: SpaciousLib
- Lệnh: /mmg
- Quyền hạn: ditmemay.mmg

## WithdrawMoneyTool
- Công dụng: thu tiền hàng loạt
- Hưỡng dẫn:
  + Dùng /wmt để thiết đặt số chia (vd số chia là 5 thì tiền của từng tài khoản sẽ bị chia cho 5)
  + /wmtaccept nếu đồng ý hoặc /wmtcancel để hủy
- Quyền hạn: wmt.use

## EnchantNangCao
PLUGIN TẠM DỪNG! DÙNG PLUGIN MỚI ĐỂ THAY THẾ: https://www.spigotmc.org/resources/enc.64871/
- Công dụng: thêm nhiều phù phép độc đáo
- Yêu cầu: SpaciousLib, EffectLib
- Hỗ trợ: KeepMyLife, DeathDropsAPI, Essentials, WorldGuard, WorldEdit
- Lệnh: 
  + /enc: mở menu
  + /enc help: xem danh sách lệnh
  + /enc list: xem toàn bộ phù phép
  + /enc add: thêm phù phép
  + /enc del: xóa phù phép
  + /enc reload: nạp lại cấu hình
- Quyền hạn:
  + enc.reload (cho /enc reload)
  + enc.add (cho /enc add)
  + enc.del (cho /enc del)

## MyKit
- Công dụng: plugin kit,sử dụng GUI
- Yêu cầu: SpaciousLib
- Lệnh:
  + /kit để mở menu kit
  + /mykit để mở menu quản lý kit
- Quyền hạn: 
  + mykit.kits.XXX (cho phép sử dụng kit có id là XXX)
  + mykit.admin (cho /mykit)

## CronJobs
- Công dụng: lập lịch chạy các tác vụ
- Yêu cầu: SpaciousLib
- Lệnh:
  + /cj để xem thông tin tác vụ
  + /cj reload để nạp lại cấu hình
- Quyền hạn: cronjobs.admin

## MultiCmdExec
- Công dụng: thực thi lệnh hàng loạt
- Lệnh: /mce (tự reload config)
- Quyền hạn: mce.admin
