# Agent Instructions

## Google Drive Build 交付規範（所有 Agent 必須遵守）
- 所有 Build 的正式目的地：Google Drive `AI Project/openselfservice/`；資料夾名稱必須與 GitHub Repo 名稱一致（AI Project ID `1Yhfro6Ss5TSCXCVIZIHEu5h7V1gL8b27`）。不可將壓縮檔散放於 `AI Project/` 根目錄，也不可每次 Build 新建頂層版本資料夾。
- **最新版直接放專案資料夾根目錄**，但需確認完整且經實際測試：ZIP／EXE、SHA-256、完整分卷與必要安裝／還原腳本一併提供；多平台最新版可並存。上傳後讀回 parent／檔名／大小／checksum，缺 ZIP 或分片的不完整新版本不能覆蓋舊的完整版本。
- **只有重大功能、架構、相容性或美術改版才在專案內建立 `vX.Y.Z-說明/`**。一般舊版移入 `歷史封存/`，保留檔案不可直接刪除。
- 新功能與修正必須提交 GitHub。昂貴 Actions 建置以 `workflow_dispatch` 或 `release: published` 受控觸發，避免每次 push main 就 Build。完成時回報 Drive 專案資料夾、版本、檔案、校驗與測試情形。
**For Codex:** Latest complete tested builds at `AI Project/openselfservice/`; archive routine old builds under `歷史封存/`; separate version folders only for significant milestones, never partial uploads.
