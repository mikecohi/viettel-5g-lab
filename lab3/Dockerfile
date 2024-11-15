FROM nginx:latest

RUN mkdir /usr/share/nginx/html/web2

COPY ./meetup/* /usr/share/nginx/html/web2/

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 8080