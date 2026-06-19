# Minecraft 服务器自动备份

每 5 天在 GitHub 云端自动运行（不依赖任何本地电脑）：
连接服务器 SFTP → 打包 → 上传到 Google Drive `mc-backups/` → 保留最新 6 份。
同时清理面板节点上多余的旧备份。

## 需要的 Secrets（仓库 Settings → Secrets and variables → Actions）

- `RCLONE_CONF_B64` — rclone 配置（含 SFTP 与 Google Drive 令牌）的 base64 编码
- `PTERO_API_KEY` — 翼龙面板 Client API 密钥（`ptlc_...`）

## 手动触发

Actions 页面 → "Minecraft Backup to Google Drive" → Run workflow。

## 修改保留份数 / 频率

见 `.github/workflows/backup.yml` 顶部的 `env` 和 `cron`。
