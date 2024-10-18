# TÔM CUA CÁ REACT JS (REACT FUNCTION COMPONENT - RFC)
Luyện sử dụng các hook lấy và đẩy data từ redux trong reactJS và xử lý nghiệp vụ trong store
## CÔNG NGHỆ SỬ DỤNG
- JavaScript
- React (Function Components)
- Redux for state management


## Xử lý nghiệp vụ
- Xác định thành phần thay đổi để tạo Store redux. Tạo store tổng gồm 3 mảng bao gồm:
    + Mảng danh sách cược: 6 con vật đặt cược có phần từ là: (mã , hình ảnh , điểm đặt dược)
    + Phần tử: Tổng điểm
    + Mảng xúc xắc : Khi ấn Xóc đĩa

- Xử lý action đặt cược trên redux:
    1. Tìm index khi click đặt cược (Copy tạo mảng mới đặt tên: danhsachDatCuocUpdate từ store state danhSachCuoc )

    2. Duyệt mảng danhsachDatCuocUpdate findIndex trả về quân cược mã trùng với mã quân cược mà action gửi lên thì thực hiện sét lại tổng thưởng và điểm cược trong store

    3. Lắc xúc xắc: Lấy phần tử trong mảng danh sách cược đẩy vào mảng xúc xắc
    + Chạy vòng lặp 3 lần kết hợp thuật toán random trả về mảng mới có 3 phần tử. => Push mảng mới vào mangXucXac để render màn hình

    4. Xử lý điểm thưởng
    5. Xử lý kết thúc ván chơi

    - Kiểm tra xem người chơi đã hết điểm hay chưa
    - Nếu hết điểm, kết thúc ván chơi và hiển thị  thông báo
    - Nếu còn điểm, cho phép người chơi tiếp tục đặt cược

    6. Xử lý lưu trữ lịch sử chơi

    - Lưu trữ thông tin về các ván chơi đã diễn ra
    - Hiển thị lịch sử chơi cho người chơi
## Công nghệ sử dụng
- JavaScript
- React (Function Components)
- Redux for state management

## Thuật toán đổ xúc xắc
- Tỉ lệ xuất hiện mỗi con vật: 100% / 6 = 16.67% (công bằng cho mỗi lựa chọn)
- Sử dụng hàm Math.random() để tạo số ngẫu nhiên và xác định kết quả

## Tỉ lệ trả thưởng
- Tỉ lệ trả lại tiền: 1:1
- Ví dụ: Nếu người chơi đặt 100 điểm vào "Tôm" và thắng, họ sẽ nhận lại 200 điểm (100 điểm cược ban đầu + 100 điểm thắng)

## Cách cài đặt và chạy dự án
1. Clone repository về máy local:
    - git clone [URL của repository]
2. Di chuyển vào thư mục dự án:
    - cd tom-cua-ca-react
3. Cài đặt các dependencies:
   - npm install
4. Chạy dự án:
   - npm start
5. Mở trình duyệt và truy cập `http://localhost:3000` để xem kết quả.

## Cấu trúc thư mục
- src/ |-- components/ | |-- BanChoi.js | |-- DanhSachCuoc.js | |-- XucXac.js |-- redux/ | |-- actions.js | |-- reducer.js | |-- store.js |-- App.js |-- index.js



## Hướng dẫn sử dụng
1. Chọn con vật muốn đặt cược (Tôm, Cua, Cá, ...)
2. Nhập số điểm muốn đặt cược
3. Nhấn nút "Đặt cược"
4. Nhấn nút "Xóc đĩa" để bắt đầu lắc xúc xắc
5. Kết quả sẽ hiển thị và điểm thưởng sẽ được tính toán tự động

## Cảm Ơn
- Dự án được thực hiện nhằm mục đích tự phát triển kỹ năng cá nhân, Trong dự án có sử dụng hoặc tham khảo thêm 1 số trang web/blog của một số cá nhân và tập thể.Xin chân thành cảm ơn ! 

