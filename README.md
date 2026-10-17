# 🎓 GRE Master Pro (GRE 智慧互動解題與學習平台)

**GRE Master Pro** 是一款專為 GRE 考生設計的單一檔案（Single-file Web App）互動解題與學習系統。本專案結合 **Vibe Coding** 開發理念，採用亮眼清爽的**學院風亮色撞色 (Bright Academic & Pop Contrast)** 設計，整合 Mason 2000 核心單字庫與同義詞資料庫，提供即時翻譯解題、系統化錯題本與翻牌單字卡功能。

---

## ✨ 核心特色 (Key Features)

### 1. ⚡ 即時解題與翻譯專區 (Real-time Solver)
* **多題型支援**：涵蓋填空 (Text Completion / Sentence Equivalence)、閱讀理解 (Reading Comprehension) 與數量推理 (Quantitative Reasoning)。
* **自動考點比對**：輸入題目後自動搜尋並匹配 Mason 2000 高頻單字，呈現字根拆解與同義詞配對。
* **一鍵收錄**：支援直接將題目與解析加入個人錯題本。

### 2. 📚 系統化錯題本 (Mistake Notebook)
* **分類篩選**：可依照「填空」、「閱讀」、「數學」及「全部」進行快速切換。
* **狀態追蹤**：支援標記「需再複習」與「已掌握」，輕鬆控管複習進度。
* **個人筆記與備份**：每道錯題皆可自由編輯 Personal Notes，並提供 JSON 格式備份下載。

### 3. 🃏 個人單字書 Deck (Vocabulary Deck)
* **3D 翻牌卡片**：預設顯示英文單字與音標，點擊卡片翻面查看中文釋義、字根與同義詞。
* **遮蓋測驗模式**：一鍵轉換為測驗模式（Flashcard Mode），方便自我檢測記憶熟練度。
* **智慧搜尋**：支援關鍵字、中文釋義或字根快速檢索。

---

## 🛠️ 技術架構 (Technical Architecture)

* **前端技術**：HTML5, CSS3 (自訂 Flexbox/Grid 學院風撞色樣式), JavaScript (ES6+)
* **圖示與字型**：FontAwesome 6.4.0, Google Fonts (Fredoka, Noto Sans TC, Playfair Display)
* **資料持久化**：使用瀏覽器原生 `window.localStorage` 儲存個人錯題本與自訂單字，重新整理或關閉頁面資料不遺失。
* **資料庫整合**：透過 Fetch API 自動讀取 `./assets/GRE_Mason_Full_Database_2.json`。

---

## 📁 檔案結構 (Project Structure)

```text
gre-master-pro/
├── README.md                            # 專案說明文件
├── index.html                           # 主系統原始碼（包含 HTML/CSS/JS）
└── assets/
    └── GRE_Mason_Full_Database_2.json   # Mason 2000 單字與同義詞資料庫
