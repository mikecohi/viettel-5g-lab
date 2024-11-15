# Lab 2
Đề bài: Triển khai deployment một ứng dụng web tĩnh lên kubernetes cho phép truy cập từ bên ngoài thông qua nodePort

Output:

• Đóng gói thành công container chứa web tĩnh

• 1 deployment chạy ứng dụng web tĩnh (replicas=2)

• 1 nodePort service trỏ tới deployment (service web 1)

• Thực hiên curl tới nodePort và cho ra kết quả trang web tĩnh theo template

## Kết quả:
```bash
kubectl logs pod/web1-df85d5c88-4t88d -n lab2
```
Trả về kết quả là: 127.0.0.1 - - [15/Nov/2024:07:02:43 +0000] "GET / HTTP/1.1" 200 37512 "-" "curl/7.88.1" cho thấy rằng 

- một yêu cầu GET / đã được gửi tới server từ địa chỉ IP 127.0.0.1 (localhost).

- HTTP Status 200 cho thấy rằng server đã trả về một phản hồi thành công.

- Kích thước của phản hồi là 37512 bytes, có thể là kích thước của trang HTML hoặc tài nguyên mà Nginx đang phục vụ.

```bash
kubectl get nodes -o wide // Lấy NodeIP: 192.168.65.3
curl curl 192.168.65.3:30030
```
Kết quả đã trả về file html của trang web tĩnh
