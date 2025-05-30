# telegram-link-redirector

`t.bibica.net` sẽ có tác dụng tương tự như `t.me`, thay thế vì các link Telegram `t.me` đã bị chặn tại Việt Nam

# Cài đặt

- [Fork](https://github.com/bibicadotnet/telegram-link-redirector/fork) repository này về tài khoản của bạn
- Triển khai lên Cloudflare Pages -> Cloudflare Workers & Pages -> importing Git repository này vào phần Pages
- Cấu hình subdomain phụ cho gọn URL

# Sử dụng
- Hỗ trợ các link dạng
```
https://t.me/+qllIQbJTrj84NDFl
https://t.me/bibica.net
https://t.me/socks?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
https://t.me/proxy?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
............
```
- ví dụ nếu bạn dùng 1 sub domain phụ `t.bibica.net`, các link `t.me` sẽ thành
```
https://t.bibica.net/+qllIQbJTrj84NDFl
https://t.bibica.net/bibica.net
https://t.bibica.net/socks?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
https://t.bibica.net/proxy?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
............
```

Ban đầu thuần túy proxy các link từ Telegram sang 1 domain mới, để tránh vấn đề nhà mạng chặn, mà hôm nay mình nhận được thông báo 

<p align="center">
  <img src="https://raw.githubusercontent.com/bibicadotnet/telegram-link-redirector/refs/heads/main/2025-05-31_03-51-47.png" alt="Demo Image" width="600"/>
</p>

Nôm na Cloudflare nhận được 1 số báo cáo, nói các link từ dịch vụ của họ là trang giả mạo, nên để đỡ lằng nhằng, các link không đúng định dạng mở ứng dụng Telegram sẽ tự chuyển về home repository này
