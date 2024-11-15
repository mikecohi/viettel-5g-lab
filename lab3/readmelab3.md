# Lab 3

**Đề bài:** triển khai nginx proxy cho nhiều ứng dụng
- từ level 2, triển khai thêm 1 trang web static thứ hai, khác với static web đã triển khai
- service cho trang web tĩnh mới được lấy tên là web2
- triển khai thêm 1 deployment nginx-proxy đóng vai trò proxy cho cả 2 ứng dụng trên và tạo
nodePort service có tên "nginx-proxy“
- thiết lập cấu hình config của nginx-proxy sao cho:
  + khi gọi tới nginx-proxy với path /web1 > nginx-proxy filter path và forward tới service web 1 >
service web1
  + khi gọi tới nginx-proxy với path /web2 > nginx-proxy filter path và forward tới service web 2 >
service web2

**Output:**
+ curl http://\<node-ip>:\<node-port>/web1 > trả về static web 1
+ curl http://\<node-ip>:\<node-port>/web2 > trả về static web 2

## Kết quả thực hành

Tạo static web thứ 2: 

![Screenshot 2024-11-15 092436](https://github.com/user-attachments/assets/1ae5eb75-3888-42f3-b0d3-e76f726786e7)

Tạo nginx-proxy, dockerize nginx-proxy rồi triển khai

![Screenshot 2024-11-15 102343](https://github.com/user-attachments/assets/c72d0eb6-9986-48d5-b4c5-853cf0824aed)
![Screenshot 2024-11-15 102748](https://github.com/user-attachments/assets/6328e941-8f09-4730-af5f-b121828c28dc)

 Dùng nginx-proxy gọi tới trang web thứ nhất:

![Screenshot 2024-11-15 103253](https://github.com/user-attachments/assets/3cd86dfe-bb40-41fd-ac15-8fe799225f71)

Curl tới trang web thứ hai:

![Screenshot 2024-11-15 103546](https://github.com/user-attachments/assets/420f28d0-2b92-4a47-b11b-cf8850dca549)
