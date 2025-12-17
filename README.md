# thursday_fiinal_project


Sheet:https://docs.google.com/spreadsheets/d/18rT0H_T6YIXXnzqdypWrF5SfGpNNPvdwvCHF5XPkP6g/edit?usp=sharing

# 🎬 觀影手帳 Pro（Movie Diary Pro）

一個結合 **AI 電影推薦 × 個人觀影資料庫 × 收藏與評分系統** 的互動式 Web App。  
透過 Gemini AI、TMDB API 與 Google Sheets，打造屬於你的智慧觀影手帳。

---

##  專案特色 Features

- 🤖 AI 智能推薦
  - 依據使用者「心情 + 喜好類型」生成電影推薦
  - 使用 Google Gemini（Generative AI）產生推薦名單
- 🎞️ 即時電影資料整合
  - 串接 TMDB API，自動取得電影簡介、評分與海報
- 🗂️ 個人觀影資料庫
  - 所有推薦電影自動儲存至 Google Sheets
  - 避免重複電影、即時同步更新
- ⭐ 收藏與個人評分系統
  - 標記 Favorite（我的最愛）
  - 自訂個人評分與短評
- 🍀 隨機幸運推薦
  - 從資料庫中抽選一部高分電影
- 📊 **我的片單總覽**
  - 以表格方式查看所有電影與個人紀錄

---

## 🛠️ 使用技術 Tech Stack

| 類別 | 技術 |
|----|----|
| 前端介面 | Gradio |
| AI 推薦 | Google Gemini API |
| 電影資料 | TMDB API |
| 資料庫 | Google Sheets |
| 後端邏輯 | Python |
| 資料處理 | Pandas |
| API 請求 | Requests |

---

## 📂 系統架構概覽

使用者輸入（心情 / 類型）
↓
Gemini AI 生成推薦電影
↓
TMDB API 查詢電影資訊
↓
Google Sheets 儲存資料
↓
Gradio 即時顯示與互動


---

## 🧠 功能說明

### 1️⃣ AI 智能推薦
- 輸入當下心情與想看的電影類型
- AI 產生 3 部推薦電影
- 系統自動：
  - 檢查是否已存在於資料庫
  - 若無則透過 TMDB 補齊資料並存入

### 2️⃣ 手氣不錯（隨機推薦）
- 從資料庫中挑選評分 ≥ 6 的電影
- 若沒有高分電影，則隨機抽取一部

### 3️⃣ 評分與收藏
- 選擇電影
- 設定：
  - ❤️ 是否加入收藏
  - ⭐ 個人評分
  - 📝 個人短評
- 資料即時寫回 Google Sheets

### 4️⃣ 我的片單總覽
- 查看所有電影
- 一覽：
  - 系統評分
  - 個人評分
  - 收藏狀態
  - 心情與類型紀錄

---

## 🔐 API 與權限設定

本專案使用以下 API Key（以 Google Colab Secrets 管理）：

- `TMDB_API_KEY`
- `GEMINI_API_KEY`

Google Sheets 使用 OAuth 方式授權，需具備存取權限。

---

## 🚀 執行方式 How to Run

1. 開啟 Google Colab
2. 安裝必要套件：
   ```bash
   pip install gradio requests google-generativeai gspread pandas



