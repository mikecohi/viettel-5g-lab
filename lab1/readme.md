# Lab 1
**Đề bài:** Triển khai deployment chạy nginx (default) lên kubernetes và cho phép truy cập từ bên ngoài thông qua nodePort

**Output:**

• 1 deployment nginx (replicas=2 pod)

• 1 nodePort service trỏ tới deployment

• thực hiên curl tới nodePort và cho ra kết quả trang web mặc định của nginx

## Kết quả

Các bước thực hiện: Tạo Deployment cho nginx > Tạo Service với NodePort > Kiểm tra và truy cập

![Screenshot 2024-11-15 113541](https://github.com/user-attachments/assets/1fbe5c1a-6976-4bc1-b74b-254f1dc5eab1)

Curl tới nodePort và cho ra kết quả trang web Mặc định của nginx:

![Screenshot 2024-11-15 113451](https://github.com/user-attachments/assets/096e03b4-4e3a-4714-a895-d26adc905b5c)
