# 電子病歷管理系統 (Electronic Health Record System)

本專案為「電子病歷」課程之期末實作作品，使用 ASP.NET Core 框架結合 SQL Server 開發。系統主要實作病人基本資料的 CRUD（新增、查詢、修改、刪除）功能，並針對醫療資訊所需的資料準確性，設計了相對應的驗證機制。

## 專案演示與文檔
* **線上簡報 (含功能演示影片)**：[Canva 連結](https://www.canva.com/design/DAGZBoczA9c/nBkBsFR5MWjY9wsRLRLIxQ/view?utm_content=DAGZBoczA9c&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hfd0f023e63)

## 核心功能
* **病人資訊維護**：實作完整的資料處理流程，包含病人資料的建立、修改與刪除。
* **CSV 檔案處理**：支援透過 CSV 檔案批次匯入病人資料，提升資料建立效率。
* **資料一致性檢查**：系統於資料輸入端即進行初步過濾，確保資料格式符合預期。

## 技術實作與個人貢獻
在團隊開發中，我主要負責「資料輸入驗證」與「重複資料提醒」邏輯，確保系統資料庫的正確性：

1. **後端資料驗證邏輯**：
   - 針對身分證字號、出生日期等關鍵欄位撰寫驗證邏輯，確保存入 SQL Server 的資料格式正確。
2. **重複資料偵測機制**：
   - 在新增病歷前，實作資料庫檢索邏輯，比對身分證字號是否已存在，避免重複建立病歷檔案造成資訊混淆。
3. **即時警告提示**：
   - 當系統偵測到資料格式錯誤或重複輸入時，實作彈出式警告視窗 (Alert) 提示使用者，優化操作流程並減少輸入錯誤。

## 開發技術棧
* **開發框架**：ASP.NET Core (C#)
* **資料庫管理**：Microsoft SQL Server Express / SSMS
* **前端技術**：HTML, CSS, JavaScript, AJAX
* **開發工具**：Visual Studio 2022
