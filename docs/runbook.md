# rectangle-formula-slides Runbook

## 開工

1. 讀取 `AGENTS.md` 與 `PROGRESS.md`。
2. 確認 `index.html` 存在；不需要安裝套件。

## 常用命令

在專案根目錄：

```sh
python3 -m http.server 8035
```

預期看到本機 HTTP server；以瀏覽器開啟 `http://127.0.0.1:8035/`。直接開啟 `index.html` 亦可播放。

驗證內嵌腳本：

```sh
node -e 'const fs=require("fs");const t=fs.readFileSync("index.html","utf8");new Function(t.match(/<script>([\\s\\S]*)<\\/script>/)[1]);console.log("script: OK")'
```

GitHub Pages 發布：在乾淨的主分支推送 `index.html`，於 GitHub repository Settings → Pages 選擇 `Deploy from a branch`、`main` 與 `/ (root)`。確認網站網址可開啟後，記入 `PROGRESS.md`。

## 排錯

- 頁面沒有內容：檢查瀏覽器 developer console 的 JavaScript 語法錯誤；先執行上述 Node 驗證命令。
- GitHub Pages 404：確認 `index.html` 位於選定來源的根目錄，並等待 Pages workflow 完成。
- 更新未顯示：確認最新 commit 已推送，並在 GitHub Pages 設定頁查看發布狀態；必要時以硬重新整理清除快取。

## 文件同步對照

| 變更 | 要檢查的文件 |
|---|---|
| 架構、資料流、schema | `docs/design/architecture.md` |
| 啟動、驗證、排錯命令 | `docs/runbook.md`、`AGENTS.md` |
| Session 結論與下一步 | `PROGRESS.md` |

## 收工

1. 執行 runbook 的 Node 腳本解析驗證，並以瀏覽器手動測試首尾頁、鍵盤切換與至少一頁差的平方／平方差圖形。
2. 核對入口、架構、runbook 與實作宣稱。
3. 更新 `PROGRESS.md`，記錄命令、結果、踩坑、決策與下一步。
4. 檢查 `git status --short`，說明未提交變更與暫存產物。
5. 依《Coding 專案文件規範》執行 fresh-context 可接手性回測。
