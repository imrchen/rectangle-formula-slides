# rectangle-formula-slides

本檔為本專案的 canonical Agent 入口。

## 專案目的

已確認：提供一份可公開發布、可離線播放的 HTML 簡報，以長方形面積圖解八上 1-1 的乘法公式。

## 目前狀態

active。16 頁靜態簡報已發布至 GitHub Pages；目前依課堂試用回饋持續調整。

## 快速啟動

不使用套件或建置工具。讀取 `AGENTS.md`、`PROGRESS.md` 後，以瀏覽器開啟 `index.html`；或在專案根目錄執行 `python3 -m http.server 8035`，瀏覽 `http://127.0.0.1:8035/`。

## 工作流程

直接修改 `index.html` 中的投影片資料、SVG 圖形或樣式；以 Node 檢查內嵌 JavaScript 可解析，並在瀏覽器檢查鍵盤與點擊切換。視覺或互動改動同步更新架構／runbook；每輪結束更新 `PROGRESS.md`。

## 主要路徑

- `index.html`：唯一的可發布靜態簡報。
- `docs/design/architecture.md`：架構與技術決策。
- `docs/runbook.md`：本機預覽、驗證與 GitHub Pages 發布流程。
- `scripts/`：目前無正式腳本。
- `tests/`、`fixtures/`、`output/`：目前不適用。

## 安全邊界

不得加入學生資料、帳號憑證、教材 PDF 或受限制的教材圖片。GitHub repository 與 Pages 網站皆為公開；推送、建立 release、變更 Pages 設定或刪除遠端內容屬外部狀態改動，須由 Roger 明確授權。本次 GitHub Pages 初次發布已獲授權。

## 文件索引

- `PROGRESS.md`
- `docs/design/architecture.md`
- `docs/runbook.md`
