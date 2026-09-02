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

## 2026-09-02 第4輪

### 啟動依據

- Roger 交辦：差的平方公式（第 9-11 頁）改用課本插圖的敘事順序並加強「撕紙條」動感；和平方／差平方之間加一張比較頁。math 工作站的 PPTX 已先更新，本輪為對應的 HTML 呈現調整，內容一致。

### 已完成

- 差的平方公式改為 3 頁新敘事：撕掉兩條 ab 紙條（動畫撕開兩條紙條，角落靜止不動）→ 角落 b² 被撕兩次（紅色脈動提示）→ 補回多扣的 b²（藍色彈入動畫）。移除原本「先扣右邊一條 ab」的單條鋪陳頁。
- 新增比較頁：(a＋b)² 與 (a－b)² 並列，凸顯唯一差別在中間項 ±2ab 的正負號，版面沿用既有兩欄樣式與色彩語言（teal／accent rose／amber 強調線）。
- 簡報總頁數由 16 頁調整為 17 頁。
- 同步更新 `AGENTS.md`、`docs/design/architecture.md`（含補齊過時的「已實現」段落）。

### 驗證

- Node 解析內嵌 JavaScript：通過；`diagram:'...'` 引用與已移除的 `diffRight`/`diffDouble`/`diffRepair` 皆已清除。
- 本機瀏覽器（`python3 -m http.server 8035`）人工檢查：第 9-12 頁動畫與版面正確、鍵盤 End 可達最後一頁（17/17）、瀏覽器 console 無錯誤。

### 下一步

- 待 Roger 課堂實際使用後回饋撕紙條動畫節奏與比較頁易讀性，再視需要微調。

### 工作區狀態

- 本輪變更尚未推送；`git status` 顯示 `index.html`、`AGENTS.md`、`PROGRESS.md`、`docs/design/architecture.md` 有未提交修改。

## 2026-09-02 第5輪

### 啟動依據

- Roger 交辦：修改 `AGENTS.md`，移除「教學內容變更需先在 math 更新 PPTX、再由 Roger 交辦同步」的強制流程，本站可獨立調整教學內容。
- Roger 提出構想並確認採用：在所有乘法公式圖解講完之後，加一張「怎麼選公式」的判斷頁，幫學生看到題目時判斷該用哪個方法。

### 已完成

- 更新 `AGENTS.md`「與 math 工作站的關係」段落：本站可獨立調整教學內容、敘事順序與呈現方式，不強制同步 math 的 PPTX。
- 新增結尾判斷頁（第 18 頁）：三張色卡分類「內容不同→老實展開」「同號→(a±b)²，正負號照抄」「異號→平方差」，各配一個示意算式，維持精簡的一眼判斷風格，不做完整例題詳解。
- 簡報總頁數由 17 頁調整為 18 頁。
- 同步更新 `docs/design/architecture.md` 頁數與測試策略描述。

### 驗證

- Node 解析內嵌 JavaScript：通過。
- 本機瀏覽器人工檢查：跳至第 18 頁版面與配色正確、console 無錯誤。

### 下一步

- 待 Roger 課堂實際使用後回饋判斷頁的分類是否清楚、要不要加更多示意算式。

### 工作區狀態

- `AGENTS.md` 的獨立作業調整已於本輪稍早 commit（`3118c3a`）。判斷頁改動（`index.html`、`docs/design/architecture.md`、本節 `PROGRESS.md`）尚未 commit。

## 2026-09-02 第6輪

### 啟動依據

- Roger 交辦：判斷頁再加幾個「心算」數字題目（203×197、9.8×10.5、303²、99²），進階題目留給習作／試卷，不在本站列出。

### 已完成

- 新增結尾第 19 頁「公式也能拿來心算」：4 張色卡，303²／99² 對應同號 (a±b)²、203×197 對應異號平方差、9.8×10.5 作為「看似整數但正負尾巴不對稱、不能套公式、要老實乘」的對照組。色卡配色沿用上一頁（第 18 頁）的 teal／rose／lav 判斷語彙，兩頁互相呼應。
- 順手修正一個 CSS 疊層問題：`.cardLabel` 原本內建 `fill:var(--ink)`，在樣式表中排在 `.teal`/`.rose` 之後，導致同時掛兩個 class 時永遠被 ink 蓋掉、標籤文字沒有真的變色。改為 `.cardLabel` 不設 fill，另建 `.ink` 工具class，讓第 18、19 頁的標籤現在能正確顯示 teal／rose 顏色。
- 簡報總頁數由 18 頁調整為 19 頁；同步更新 `AGENTS.md`、`docs/design/architecture.md` 頁數與測試策略描述。

### 驗證

- Node 解析內嵌 JavaScript：通過。
- 手算覆核心算範例：303²=91809、99²=9801、203×197=39991、9.8×10.5=102.9，均與投影片內容一致。
- 本機瀏覽器人工檢查：第 18、19 頁版面、配色（含修正後的標籤顏色）正確，console 無錯誤。

### 下一步

- 待 Roger 課堂實際使用後回饋這兩張判斷／心算頁是否需要調整例子或順序。

### 工作區狀態

- 本輪變更（`index.html`、`AGENTS.md`、`docs/design/architecture.md`、本節 `PROGRESS.md`）尚未 commit。

## 2026-09-02 第7輪

### 啟動依據

- Roger 交辦：第 18、19 頁對調（心算範例在前、代數判斷在後，先具體後抽象）；第一頁加一點視覺調整讓人更清楚知道這是首頁。

### 已完成

- 對調第 18、19 頁順序：「公式也能拿來心算」移到第 18 頁，「看到題目，怎麼選公式？」移到第 19 頁（收尾）。
- 首頁（title-slide）加上柔和薄荷綠底色漸層，與其他頁的純白背景區隔；「按 → 或空白鍵開始」改成 teal 圓角按鈕樣式，更明確標示這是起始頁與操作方式。其他頁面樣式不受影響。
- 同步調整 `docs/design/architecture.md` 測試策略裡兩頁的描述順序。

### 驗證

- Node 解析內嵌 JavaScript：通過。
- 本機瀏覽器人工檢查：第 18／19 頁內容對調正確、首頁底色與按鈕樣式正確、其餘頁面未受影響、console 無錯誤。

### 下一步

- 待 Roger 課堂實際使用後回饋整體頁序與首頁觀感。

### 工作區狀態

- 本輪變更待 commit、push。
