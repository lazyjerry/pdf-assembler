# PDF Assembler

**PDF Assembler** 是一個基於網頁的工具，讓你可以直接在瀏覽器中合併多個 PDF 文件為單一文件。專案使用 HTML、CSS (Bootstrap 5) 與 JavaScript 開發，結合了 PDF-LIB 來處理 PDF 文件合併，並利用 SortableJS 實現拖曳排序檔案。這個專案非常適合部署在 Cloudflare Pages 上，實現靜態網站的快速上線。

## 功能特色

- **拖曳/點擊上傳：** 支援拖曳 PDF 文件至上傳區域，或點擊選擇檔案。
- **動態檔案列表：** 顯示已上傳檔案，並提供順序編號與拖曳排序功能。
- **刪除檔案：** 每筆檔案旁均有刪除按鈕，可隨時移除不需要的檔案。
- **動態檔名：** 合併 PDF 時可自行輸入檔名，若留空則預設以當前年月日（YYYY-MM-DD）作為檔案名稱。
- **即時狀態提示：** 提供上傳、刪除、排序、合併與下載等操作的即時狀態訊息。

## 線上示範

待部署後，你可透過 Cloudflare Pages 的網址預覽線上效果  
*(部署後請將此連結更新為實際網址)*

## 安裝與使用說明

### 前置需求

- GitHub 帳號
- Cloudflare 帳號（需具備 Cloudflare Pages 權限）
- 基本的 HTML、CSS 與 JavaScript 知識

### 安裝步驟

1. 使用 Git 下載專案：

   ```bash
   git clone https://github.com/lazyjerry/pdf-assembler.git
   cd pdf-assembler
   ```

2. 在本機端開啟 `index.html` 測試效果（直接用瀏覽器開啟即可）。

### 部署至 Cloudflare Pages

1. **建立 Cloudflare Pages 專案：**
   - 登入 [Cloudflare Dashboard](https://dash.cloudflare.com/)。
   - 點選 **Pages** 並點擊 **Create a project**。
   - 連結 GitHub 帳號，選擇 `pdf-assembler` repository。

2. **設定建置參數：**
   - **Framework preset：** 選擇 **None**（因為這是一個純靜態網站）。
   - **Build command：** 如果不使用前端框架或打包工具，可留空。
   - **Build output directory：** 設定為存放 `index.html` 的目錄（通常為 repository 根目錄）。

3. **部署：**
   - 點選 **Save and Deploy**，Cloudflare Pages 將自動建置並部署網站，你將會收到一個線上連結。

## 使用方法

- **上傳 PDF 文件：**  
  拖曳 PDF 文件至上傳區域，或點擊上傳區域開啟檔案選擇器。

- **調整檔案順序：**  
  檔案列表中每筆項目左側的拖曳圖示（☰）可用於調整順序，列表會自動顯示順序編號（如 #1、#2）。

- **刪除不需要的檔案：**  
  點擊每筆檔案右側的垃圾桶圖示（🗑️）即可移除該檔案。

- **合併 PDF：**  
  輸入合併後的 PDF 檔名（若留空，系統將自動使用當前日期 YYYY-MM-DD），然後點擊 **合併 PDF** 按鈕開始合併。

- **下載 PDF：**  
  合併完成後，點選 **下載 PDF** 按鈕下載合併後的檔案。

## 技術使用

- **PDF-LIB：** 用於客戶端處理與合併 PDF 文件。
- **SortableJS：** 實現檔案列表的拖曳排序功能。
- **Bootstrap 5：** 用於網頁響應式設計與樣式美化。
- **HTML、CSS 與 JavaScript：** 建置整體前端功能。

## 貢獻指南

歡迎任何形式的貢獻！如果有建議或錯誤回報，請提交 issue 或直接提出 pull request。

## 授權條款

本專案採用 MIT License 授權，詳情請參閱 [LICENSE](LICENSE) 文件。

## 聯絡資訊

如有任何疑問或建議，請於 [GitHub Issues](https://github.com/lazyjerry/pdf-assembler/issues) 中反映，或直接聯絡 [lazyjerry](https://github.com/lazyjerry)。
