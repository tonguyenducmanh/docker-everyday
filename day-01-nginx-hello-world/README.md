## Test host 1 static html bằng Nginx docker container

chạy lệnh sau để có thể build được image từ docker file

```
docker build -t hehe-nginx .
```

chạy lệnh sau để có thể khởi tạo được 1 container từ file image

```
docker run -it --rm --name some-nginx -d -p 1234:80 hehe-nginx
```

truy cập vào đường dẫn sau để xem được nginx tạo thành công hay chưa

```
http://localhost:1234/
http://localhost:1234/hehe.html
```

để ngừng container vừa tạo

```
docker stop some-nginx
```

xóa cache build những lần trước từ docker

```
docker container prune -f
```
