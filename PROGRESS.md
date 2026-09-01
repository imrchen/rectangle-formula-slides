# rectangle-formula-slides 進度

## 2026-09-01 第1輪（14:13）

### 啟動依據

- 《新專案啟動規範》，`modified: 2026-08-18`
- 《Coding 專案文件規範》，`modified: 2026-08-09`

### 本輪目標

- 建立最小啟動文件，完成 preflight gate，之後移入既有 HTML 簡報並發布 GitHub Pages。

### 已完成

- 建立專案目錄與啟動文件骨架。
- 已確認目的、範圍與 GitHub 帳號：`imrchen`。
- 啟動 gate 通過後，移入 16 頁零相依 HTML 簡報與公開 README。
- 建立公開 repository：`https://github.com/imrchen/rectangle-formula-slides`。
- 啟用 GitHub Pages，網址：`https://imrchen.github.io/rectangle-formula-slides/`。

### 驗證

- `check-project-start.sh --type coding --target /Users/roger/estudio/rectangle-formula-slides`：通過。
- Node 解析 `index.html` 的內嵌腳本：通過，確認 16 頁。
- GitHub Pages 狀態：`built`；公開網址回應 HTTP 200。

### 未定事項

- 初次發布後是否要設定自訂網域：未定；本輪使用 GitHub 預設網址。

### 下一步

- 視課堂試用回饋調整文字、圖形比例或逐頁節奏；每次修改 `index.html` 後推送 `main`，GitHub Pages 會重新發布。

### 工作區狀態

- Git 已初始化；已建立啟動文件 commit 與 HTML 簡報 commit。待提交本次發布紀錄更新。

## 2026-09-01 第2輪（14:26）

### 已完成

- 在每頁左下角加入低對比的小字：`桃園市光明國中 - 810 數學課 (c)`。
- 更新 `AGENTS.md` 的部署狀態。

### 驗證

- Node 解析內嵌 JavaScript：通過；頁尾標記存在。
- GitHub Pages 狀態：`built`；公開頁面已讀取到頁尾標記。

### 下一步

- 依課堂試用回饋持續調整；同一份乘法公式簡報在本專案維護，新的獨立簡報另開專案。

### 工作區狀態

- 本輪視覺更新已推送；待提交驗證紀錄。

## 2026-09-01 第3輪（14:43）

### 已完成

- 記錄跨專案分工：math 的 PPTX 是教學內容主版本；本站是公開播放用 HTML 衍生版。
- 記錄雙軌現場策略：Google Drive 上的 PPTX 與 GitHub Pages 並行，主策略待 Roger 實測後決定。

### 下一步

- 教學內容變更先回到 math；只有 Roger 明確交辦同步時才更新本站的 HTML。

### 工作區狀態

- 待提交跨專案規則更新。
