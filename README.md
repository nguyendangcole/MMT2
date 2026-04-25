# TASK1 - VLAN


- Kết nối giữa các PC cùng VLAN.
- Kết nối giữa các PC khác VLAN.
- dùng ACL để chặn 2 VLAN với nhau

| 📂 Tài liệu                | Nội dung chính                                                                 |
|----------------------------|--------------------------------------------------------------------------------|
| [⚙️ Workflow](./document/VLAN.md)         | MỤC TIÊU Tạo 3 VLAN (VLAN10, VLAN20, VLAN30) |
| [⚙️ design](./design.png)         | MỤC TIÊU thiết kế |


```C++
| PC  | VLAN | IP Address    | Default Gateway |
| --- | ---- | ------------- | --------------- |
| PC1 | 10   | 192.168.10.10 | 192.168.10.1    |
| PC2 | 10   | 192.168.10.11 | 192.168.10.1    |
| PC3 | 20   | 192.168.20.10 | 192.168.20.1    |
| PC4 | 30   | 192.168.30.10 | 192.168.30.1    |
-------------------------------------------------------------
# Gửi Tin nhắn
|         | PC1(V10) | PC2(V10) | PC3(V20) | PC4(V30) |
| ------- | -------- | -------- | -------- | -------- |
| PC1     | -        | ✔        | ✔        | ✖        |
| PC2     | ✔        | -        | ✔        | ✖        |
| PC3     | ✔        | ✔        | -        | ✔        |
| PC4     | ✖        | ✖        | ✔        | -        |
```

![](./result.png)

---
<p align="center">
  <a href="https://www.facebook.com/Shiba.Vo.Tien">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"/>
  </a>
  <a href="https://www.tiktok.com/@votien_shiba">
    <img src="https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white" alt="TikTok"/>
  </a>
  <a href="https://www.facebook.com/groups/khmt.ktmt.cse.bku?locale=vi_VN">
    <img src="https://img.shields.io/badge/Facebook%20Group-4267B2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook Group"/>
  </a>
  <a href="https://www.facebook.com/CODE.MT.BK">
    <img src="https://img.shields.io/badge/Page%20CODE.MT.BK-0057FF?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook Page"/>
  </a>
  <a href="https://github.com/VoTienBKU">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>