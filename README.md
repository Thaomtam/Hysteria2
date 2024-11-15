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
**Install SSL Commo Name**
```
mkdir -p /etc/ssl && openssl ecparam -genkey -name prime256v1 -out /etc/ssl/private.key && openssl req -new -x509 -days 3650 -key /etc/ssl/private.key -out /etc/ssl/cert.pem -subj "/CN=bing.com"
```
**Install SSL Domain**
'''
apt install -y socat
curl https://get.acme.sh | sh
source ~/.bashrc
acme.sh --upgrade --auto-upgrade
acme.sh --set-default-ca --server letsencrypt

acme.sh --issue -d EXAMPLE.COM --standalone --keylength ec-256

acme.sh --install-cert -d EXAMPLE.COM --ecc \
--fullchain-file /etc/ssl/private/fullchain.cer \
--key-file /etc/ssl/private/private.key

chown -R nobody:nogroup /etc/ssl/private
```
**Cấu hình máy chủ**
```
[Youtube](https://www.youtube.com/@kienthucandroid)
```
**Cấu Hình Máy Khách**
```
[Youtube](https://www.youtube.com/@kienthucandroid)
```
**Nhảy Cổng**
```
apt install iptables-persistent
```
```
iptables -t nat -A PREROUTING -p udp --dport 20000:40000 -j DNAT --to-destination :8443
```
```
ip6tables -t nat -A PREROUTING -p udp --dport 20000:40000 -j DNAT --to-destination :8443
```
```
netfilter-persistent save
```
```
iptables -t nat -nL --line
```
**Thaomtam**
+ **Link kênh** [Telegram](https://t.me/ktandroidreview)
+ **Link kênh** [Youtube](https://www.youtube.com/@kienthucandroid)
