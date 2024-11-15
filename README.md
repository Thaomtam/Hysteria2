# Hysteria2 x Tcp Brutal
**Lời nói đâu**
* Lần đầu tôi kéo wifi Viettel, tôi biết được rằng ở cái hẻm của tôi cái port tổng của cáp quang Viettel có 10 port tức là 10 đường truyền với các ppoe xác thực người dùng, khi đó tôi nghĩ làm cách nào để tăng tốc wifi của mình những giờ cao điểm, sau một thời gian tìm hiểu và thử nghiệm tôi đã có cách mà không cần quay PPOE, đó là dùng TCP Brutal + Hysteria 2 (Đó là sự tàn bạo của udp,người khác yếu kệ họ mình mạnh là được😄)
* Cách thực hiện :
* * 1 Server VPS
  * 2 Config
**Install Sing-Box**
```
bash <(curl -fsSL https://sing-box.app/deb-install.sh)
```
**Install TCP Brutal**
```
bash <(curl -fsSL https://tcp.hy2.sh/)
```
**Install SSL**
```
mkdir -p /etc/ssl && openssl ecparam -genkey -name prime256v1 -out /etc/ssl/private.key && openssl req -new -x509 -days 3650 -key /etc/ssl/private.key -out /etc/ssl/cert.pem -subj "/CN=bing.com"
```
```
chown -R nobody:nogroup /etc/ssl
```
**Config Server**
```
```
**Cấu Hình Máy Khách**
```
```
**Thaomtam**
