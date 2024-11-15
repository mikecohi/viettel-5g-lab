FROM nginx:latest

# Tạo thư mục chứa website
RUN mkdir /usr/share/nginx/html/web1

# Sao chép website tĩnh vào thư mục
COPY ./hook-master/* /usr/share/nginx/html/web1/

# Sao chép file cấu hình nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Expose port 8080
EXPOSE 8080