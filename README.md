# GRE Master Pro 🎓

**GRE Master Pro** 是一款專為 GRE 考生打造的智慧 AI 解題助手與備考工具。透過整合 **Google Gemini API** 與 **Mason GRE 字庫**，提供繁體中文逐空解析、句構剖析、語意轉折分析、數學驗算與智慧錯題本功能。

---

## 🌟 核心功能

### 1. 🤖 AI 智慧解題助手 (Solver)
- **多題型支援**：支援填空題（Text Completion / Sentence Equivalence）、閱讀理解（Reading Comprehension）與數量推理（Quantitative Reasoning）。
- **圖文雙模態輸入**：可直接貼上題目文字，或上傳/剪貼（Ctrl+V）題目截圖進行辨識與解析。
- **繁體中文專業解析**：
  - **填空題**：分析線索詞（Clue）、轉折關係（Direction）、句構分析與排除選項理由。
  - **數量推理**：進行詳細計算過程推導與邏輯驗算。
  - **診斷盲點**：若輸入「我的答案」，AI 會精準指出考生的思考誤區。
- **自動翻譯與單字對照**：提供整題通順中文翻譯，並自動抽取高頻單字/片語。

### 2. 📖 Mason 字庫自動比對
- 系統內建/自動載入 `GRE_Mason_Full_Database` 字典庫。
- AI 解題時會自動檢索題目關鍵字，優先套用 Mason 字庫的解釋、字根（Root）與常見同義字（Synonyms）。

### 3. 📝 個人化錯題本 (Mistake Notebook)
- **一鍵收錄**：解析完成後可直接將題目與 AI 解析歸檔至錯題本。
- **狀態管理**：提供「需再複習」與「已掌握」篩選標籤，並支援自訂個人筆記。
- **資料備份**：支援將錯題本與單字庫匯出為 JSON 檔案進行備份。

### 4. 🃏 智慧單字卡 (Vocab Flashcards)
- **卡片翻轉測試**：支援雙面單字卡（正面顯示單字/詞性，背面顯示中文/字根/同義字）。
- **一鍵全部翻面**：方便自我測驗。
- **關鍵字搜尋**：可針對單字、中文釋義或字根進行即時過濾。

---

## 🛠️ 技術架構

- **前端**：純 HTML5 + CSS3 (Neo-brutalism 新粗獷主義視覺風格) + Vanilla JavaScript (無框架依賴)。
- **AI 介接**：Google Gemini REST API (`gemini-3.8-flash` / `gemini-3.1-pro-preview`)。
- **資料儲存**：全本地端儲存 (`localStorage`)，無後端資料庫負擔，嚴格保護使用者隱私與 API Key 安全。
- **結構化輸出**：使用 JSON Schema 強制規範 AI 回傳格式。

---

## 📁 檔案結構 (Project Structure)

```text
gre-master-pro/
├── README.md                            # 專案說明文件
├── index.html                           # 主系統原始碼（包含 HTML/CSS/JS）
└── assets/
    └── GRE_Mason_Full_Database_2.json   # Mason 2000 單字與同義詞資料庫
