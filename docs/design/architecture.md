# rectangle-formula-slides 架構

## 專案目的與邊界

本專案服務教師的課堂投影：以固定位置的長方形圖形和簡短公式，協助講解八上 1-1 的分配律、括號乘法、和差平方與平方差公式。它接手 math 工作站的 HTML 原型；math 工作站保留教材研究與試作，本站只保存可公開發布的成品。

## 已實現

- 啟動文件骨架。

## 已決定尚未實作

- 單檔、零相依的 `index.html`；內容、SVG 圖形、樣式與鍵盤導覽皆封裝其中。
- 共 16 頁；右側為放大的 SVG 面積圖，左側為較小標題與醒目的關鍵公式。
- 發布到 GitHub Pages 的 repository 根目錄。

## 明確排除

- 不使用伺服器、資料庫、登入或追蹤：教室投影不需要，亦避免蒐集資料。
- 不放入教材 PDF、PPTX、學生資料或需要授權的素材：公開 repository 不適合保存這些內容。
- 不取代原始 PowerPoint：HTML 是獨立的播放版本。

## 執行環境

任何現代瀏覽器即可播放；本機預覽可使用 Python 3 的內建 HTTP server。發布服務為 GitHub Pages；沒有 dependency manager 或建置步驟。

## 架構與資料流

`index.html` 的 `slides` 陣列保存每頁文字、公式與圖形種類。`diagram` 物件產生可重用的內嵌 SVG，CSS 控制 16:9 版面與轉場，JavaScript 管理鍵盤、點擊、頁碼和進度條。唯一輸出是瀏覽器呈現的投影片。

## 技術決策

- 使用原生 HTML/CSS/JavaScript：可雙擊離線開啟，也可直接由 GitHub Pages 託管。
- 使用 SVG：數學圖形和標記保持清晰，並能在每頁維持相同位置。
- 使用 GitHub Pages：純靜態檔案不需伺服器，更新可經 Git commit 留下版本紀錄。

## 資料契約

發布根目錄必須含 `index.html`。每張投影片物件需有 `title`、`hint`、`formula`、`diagram`；`diagram` 必須對應 `diagram` 物件的函式名稱。支援方向鍵、空白鍵、PageUp/PageDown、Home/End 與點擊畫面切換。

## 已知限制

- 數學式以 Unicode 與系統字型呈現，字型外觀依裝置略有差異。
- 沒有個別投影片的可分享網址；目前只支援線性播放。
- GitHub Pages 發布後會公開可見，不能拿來存放敏感或受限制內容。

## 測試策略

以 Node 對內嵌 JavaScript 執行語法解析，並確認投影片物件數量為 16。人工於桌面瀏覽器檢查首尾頁、差的平方頁、平方差頁與鍵盤導覽；手機版採響應式單欄顯示。
