# backup-2026-08-24-1903.zip 分块说明

## 文件信息

- 原文件：`backup-2026-08-24-1903.zip`
- 大小：约 1.3 GB（1291543136 字节）
- SHA256：`08a28bb5b5fd091fde56e3d0127c10680c98567c05d40d0cae48d5d933091911`
- 来源：Google Drive（文件 ID `1XvXKO0OkL8pNis2Zr0EQoha7mZKX4Grp`）

## 为什么分块

GitHub 单个文件超过 100MB 会被拒收，因此将原文件拆成 13 个分块，
每个约 95MB（最后一个 92MB），命名为：

```
backup-2026-08-24-1903.zip.part-aa
backup-2026-08-24-1903.zip.part-ab
...
backup-2026-08-24-1903.zip.part-am
```

分块已校验：按顺序拼接后的 SHA256 与原文件一致。

## 下载与合并方法

1. 下载全部 13 个分块到同一个文件夹（顺序不能乱，文件名中的 aa、ab……am 即顺序）。
2. 合并：
   - Linux / macOS：
     ```
     cat backup-2026-08-24-1903.zip.part-* > backup-2026-08-24-1903.zip
     ```
   - Windows（cmd）：
     ```
     copy /b backup-2026-08-24-1903.zip.part-aa+backup-2026-08-24-1903.zip.part-ab+... backup-2026-08-24-1903.zip
     ```
     （13 个文件名用 `+` 连接，一次写完）
3. 校验合并结果（可选但推荐）：
   ```
   sha256sum backup-2026-08-24-1903.zip
   ```
   应输出 `08a28bb5b5fd091fde56e3d0127c10680c98567c05d40d0cae48d5d933091911`。
4. 用解压软件正常解压即可。
