# 在 Mac 上使用 Docker 建構 Laravel 環境

## Docker 建構

### Docker up

```
sudo docker-compose up -d nginx mariadb workspace php-fpm docker-in-docker phpmyadmin redis
```

### 更改 MariaDB 登入密碼

```
docker run -d \ --name mariadb-1 \ -p 3306:3306 \ -e MARIADB_ROOT_PASSWORD=root \ laradock-mariadb
```

### Docer start

<img width="1440" alt="截圖 2025-01-05 下午2 09 39" src="https://github.com/user-attachments/assets/5c0a5fc9-2656-4291-9f80-37ed7eb10f34" />


## DataBase 建構

<img width="1440" alt="截圖 2025-01-05 下午2 10 29" src="https://github.com/user-attachments/assets/7ffadd5a-7135-45bc-8cbe-ee1edd78278d" />

## Nginx 建構

### Nginx sites project config (in workspace)

<img width="530" alt="截圖 2025-01-05 下午2 14 16" src="https://github.com/user-attachments/assets/8573006b-e0dc-4fa7-9f5c-e6be305e34bb" />

### /etc/hosts 新增本地端連結

<img width="483" alt="截圖 2025-01-05 下午2 15 54" src="https://github.com/user-attachments/assets/6c94bb2f-1b61-4397-a1e7-5e3e0612eca3" />

### 網頁開啟

<img width="1440" alt="截圖 2025-01-05 下午2 10 53" src="https://github.com/user-attachments/assets/778bb3d0-92ed-4c09-badb-1d052eab3739" />

## php 版本

<img width="473" alt="截圖 2025-01-05 下午2 11 27" src="https://github.com/user-attachments/assets/1a2d5077-643e-448f-b4d7-925fe6ce167c" />

## Laravel 版本

<img width="437" alt="截圖 2025-01-05 下午2 12 29" src="https://github.com/user-attachments/assets/e0d11ba3-9c3e-4925-8588-e7e8b8dce27e" />






## 問題紀錄

### 出現此錯誤視窗，代表 docker_compose.yaml 格式不正確

<img width="1064" alt="截圖 2025-01-05 晚上10 23 14" src="https://github.com/user-attachments/assets/f0d2b5e2-8b35-4c4c-acbb-ba0739942d45" />

## 網頁出現 502 Bad GateWay，代表 Nginx 的 fastcgi_pass 沒有指到 Laradock 的 php-fpm

<img width="538" alt="截圖 2025-01-05 晚上11 26 25" src="https://github.com/user-attachments/assets/9e26b1be-1210-40a5-8134-859253a1b7b7" />


