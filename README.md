# PDF Assembler

**PDF Assembler** 是一個基於網頁的工具，讓你可以直接在瀏覽器中合併多個 PDF 文件為單一文件。專案使用 HTML、CSS (Bootstrap 5) 與 JavaScript 開發，結合 PDF-LIB 來處理 PDF 文件合併，並利用 SortableJS 實現拖曳排序檔案。這個專案非常適合部署在 Cloudflare Pages 上，實現靜態網站的快速上線。

## 功能特色

- **拖曳/點擊上傳：** 支援拖曳 PDF 文件至上傳區域，或點擊選擇檔案。
- **動態檔案列表：** 顯示已上傳檔案，並提供順序編號、拖曳排序與刪除功能。
- **動態檔名：** 合併 PDF 時可自行輸入檔名，若留空則預設以當前日期（YYYY-MM-DD）作為檔案名稱。
- **即時狀態提示：** 提供上傳、刪除、排序、合併與下載等操作的即時狀態訊息。

## 線上示範

部署後，您可以透過 Cloudflare Pages 的網址預覽線上效果：  
https://pdf-assembler.pages.dev/

## 安裝與使用說明

### 前置需求

- GitHub 帳號
- Cloudflare 帳號（需具備 Cloudflare Pages 權限）
- 基本的 HTML、CSS 與 JavaScript 知識

### 取得專案

在部署前，請先**clone** 或 **fork** 此 GitHub Repository，並確保您有權限使用與修改程式碼：

```bash
git clone https://github.com/lazyjerry/pdf-assembler.git
```

或在 GitHub 網頁上點選 **Fork**，將此專案複製到您的帳號下。

### 本地測試

1. 進入專案資料夾：
   ```bash
   cd pdf-assembler
   ```
2. 直接用瀏覽器開啟 `index.html` 測試效果。

### 部署至 Cloudflare Pages

1. **建立 Cloudflare Pages 專案：**
   - 登入 [Cloudflare Dashboard](https://dash.cloudflare.com/)。
   - 點選 **Pages** 並點擊 **Create a project**。
   - 連結您的 GitHub 帳號，並選擇您剛剛 **clone** 或 **fork** 的 Repository。

2. **設定建置參數：**
   - **Framework preset：** 選擇 **None**（此專案為純靜態網站）。
   - **Build command：** 若無前端打包需求可留空。
   - **Build output directory：** 設定為存放 `index.html` 的目錄（通常為 repository 根目錄）。

3. **部署：**
   - 點選 **Save and Deploy**，Cloudflare Pages 將自動建置並部署您的網站，並生成一個線上連結。

### 手動上傳 HTML 至 Cloudflare Pages

如果您不想使用 GitHub Repository 部署，也可手動上傳 HTML 檔案：

1. 將專案中所有檔案打包成 zip 壓縮檔（包含 `index.html`、CSS、JavaScript 等）。
2. 登入 [Cloudflare Dashboard](https://dash.cloudflare.com/)，並進入 Cloudflare Pages 頁面。
3. 選擇 **Manual Upload**（手動上傳）方式，然後上傳剛才打包的 zip 檔。
4. Cloudflare Pages 會解壓並部署您的靜態網站，完成後會提供一個線上連結。

## 使用方法

- **上傳 PDF 文件：**  
  拖曳 PDF 文件至上傳區域，或點擊上傳區域開啟檔案選擇器。

- **調整檔案順序：**  
  檔案列表中每筆項目前的拖曳圖示（☰）可用於調整順序，列表會顯示順序編號（如 #1、#2）。

- **刪除不需要的檔案：**  
  點擊每筆檔案右側的垃圾桶圖示（🗑️）即可移除該檔案。

- **合併 PDF：**  
  輸入合併後的 PDF 檔名（若留空，系統會自動使用當前日期 YYYY-MM-DD），然後點擊 **合併 PDF** 開始合併。

- **下載 PDF：**  
  合併完成後，點選 **下載 PDF** 按鈕下載合併後的檔案。

## 技術使用

- **PDF-LIB：** 客戶端處理與合併 PDF 文件。
- **SortableJS：** 實現檔案列表的拖曳排序功能。
- **Bootstrap 5：** 提供響應式設計與樣式美化。
- **HTML、CSS 與 JavaScript：** 建置整體前端功能。

## 貢獻指南

歡迎任何形式的貢獻！如果有建議或錯誤回報，請提交 issue 或直接發送 pull request。

## 授權條款

本專案採用 MIT License 授權，詳情請參閱 [LICENSE](LICENSE) 文件。

## 聯絡資訊

如有任何疑問或建議，請於 [GitHub Issues](https://github.com/lazyjerry/pdf-assembler/issues) 中反映，或直接聯絡 [lazyjerry](https://github.com/lazyjerry)。
