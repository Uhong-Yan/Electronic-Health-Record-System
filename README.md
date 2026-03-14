# 電子病歷管理系統 (Electronic Health Record System)

本專案為「電子病歷」課程之期末實作作品，使用 ASP.NET Core 框架結合 SQL Server 開發。系統成功實作了病人基本資料的完整運維流程，並針對實際醫療情境中的資料輸入需求，加入批次匯入與驗證提醒功能。

## 專案演示與文檔
由於本專案之核心功能（如資料重複警示、CSV 匯入流程）包含動態操作，**請務必點擊下方連結至線上簡報觀看演示影片**：

*  **[簡報連結 (含功能演示影片)](https://www.canva.com/design/DAGZBoczA9c/nBkBsFR5MWjY9wsRLRLIxQ/view?utm_content=DAGZBoczA9c&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hfd0f023e63)**
    > *註：進入 Canva 連結後，點擊簡報頁面中的播放鈕即可觀看功能操作實錄。*
*  **[專案 PDF)](Project_Report_EHR_System.pdf)**

## 核心功能
* **病人資訊維護 (CRUD)**：實現病人資料的新增、清單查詢、資料修改與記錄刪除。
* **CSV 數據匯入**：支援透過外部 CSV 檔案批次導入病人資訊，並實作後端資料解析與寫入。
* **資料品質控管**：系統具備基礎的欄位驗證與重複資料偵測機制。

## 技術實作與個人貢獻
在團隊開發中，我主要負責「資料輸入驗證」與「重複資料提醒」的邏輯實作：

1. **重複資料偵測**：
   - 實作資料庫檢索邏輯，在新增病歷前自動比對「身分證字號」是否已重複。
2. **即時驗證提醒**：
   - 當偵測到重複資料或欄位輸入錯誤時，實作彈出式警告視窗 (Alert) 提示使用者，確保資料唯一性並減少人工輸入錯誤。
3. **介面操作優化**：
   - 參與病人資訊清單與編輯頁面的介面配置，確保操作流程直觀。

## 開發技術棧
* **開發框架**：ASP.NET Core (C#)
* **資料庫管理**：Microsoft SQL Server Express / SSMS
* **前端技術**：HTML, CSS, JavaScript, AJAX
* **開發工具**：Visual Studio 2022
