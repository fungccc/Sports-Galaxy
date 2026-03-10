# 🌌 SPORTS GALAXY : Anatomy Master

An interactive 3D tool to learn biomechanics and anatomy across multiple sports.
這是一個涵蓋多項運動專項（包含跑步、籃球、重訓、瑜伽等 17 種項目）的 3D 解剖學互動學習系統。

## 🚀 Live Demo (立即試用)
👉 **[Click here to start / 點擊開始使用](https://fungccc.github.io/Sports-Galaxy/)**

## ✨ Core Modules (核心模組)

* **🪐 3D Galaxy Menu (星球選單):** Interactive 3D spherical menu to explore and select your training sport. (視覺化的 3D 互動球體選單，可拖曳旋轉選擇運動項目)
* **📖 Anatomy Atlas (解剖圖鑑):** A searchable, filterable visual database of anatomical structures specific to the chosen sport. (針對各專項打造的解剖圖鑑，支援即時搜尋與標籤過濾)
* **🎯 Anatomy Quiz (解剖測驗):** Customizable time challenges (5m, 15m, Infinite) based on specific body parts, functions, or sports. (可依照部位、功能自訂範圍的限時測驗挑戰)

## 🛠️ Key Features (特色功能)

* **Bilingual UI & Voice (雙語介面與發音):** Seamlessly switch between English and Traditional Chinese, complete with Text-to-Speech support. (支援中英雙語介面切換，並內建語音朗讀功能)
* **Auto Play & Blind Modes (懶人與聽力模式):** Hands-free auto-play mode for easy listening, and image-hidden dictation mode for advanced learning. (全自動播放的懶人聽書模式，以及隱藏圖片的聽音辨位測驗)
* **Smart Review (錯題複習機制):** Automatically tracks mistakes for focused review sessions. (自動記錄錯題，提供專屬的針對性複習模式)
* **Data Manager (資料管理員):** Easily import custom JSON data via text, local file, or URL. (支援透過文字、檔案或網址匯入自訂的 JSON 擴充題庫)

* ## 📁 How to Add Custom Data (如何新增自訂題庫)

The app dynamically loads JSON data based on the selected sport. All data files must be placed in the `db/` directory.
系統會根據選擇的運動項目自動讀取對應的 JSON 題庫，所有題庫檔案必須放在 `db/` 資料夾內。

### 1. File Naming (檔案命名規則)
Format: `anatomy_data_{SportName}.json`
Example: `db/anatomy_data_Boxing.json`
*(Note: The first letter of the sport name should be capitalized. 注意：運動名稱首字母需大寫)*

### 2. JSON Structure (資料格式)
Each file should contain a JSON array of objects. Here is the required structure:
每個檔案內須包含一個 JSON 陣列，單筆資料的格式如下：

```json
[
  {
    "id": "m01",
    "name_en": "Gluteus Maximus",
    "name_zh": "臀大肌",
    "tags": ["髖部與大腿", "下肢推", "伸展", "原動肌"],
    "img": "[https://example.com/image.png](https://example.com/image.png)",
    "desc": "人體最大肌肉，負責髖關節伸展。 (中文描述)",
    "desc_en": "The largest muscle in the body, responsible for hip extension. (英文描述)",
    "img_source": "圖片來源：Wikimedia Commons"
  }
]
```
### 3. Fields Explanation (欄位說明)
* **id: Unique identifier (唯一識別碼).

* **name_en / name_zh: Muscle/bone name in English and Chinese (中英文學名).

* **tags: Array of strings used for filtering in the Atlas and Quiz. Matches taxonomy like body parts, functions, etc. (用於分類過濾的標籤陣列，對應解剖位置或動作功能).

* **img: URL of the anatomical image (圖片網址).

* **desc / desc_en: Detailed explanation in both languages (雙語詳細解說).

* **img_source: (Optional) Credit for the image (圖片版權來源標示).
