

upstream backend {
    server backend1.example.com weight=5;
    server backend2.example.com;
    server 192.0.0.1 backup;
}
backup -> 非 backup 全掛, 使用


Load Balancing Method
1 round-robin (預設) 搭配 weight
2 least_conn 最少活動
3 ip_hash 同一地址的請求至同一服務器

服務器慢啟動
會話持久性
配置健康檢查
