# 香港仔隧道巴士轉乘站 PIDS 模擬器
# Aberdeen Tunnel BBI PIDS Simulator

一個基於香港政府資料一線通（DATA.GOV.HK）城巴（Citybus）開放 API 構建的香港仔隧道巴士轉乘站乘客資訊顯示屏（Passenger Information Display System, PIDS）模擬器。

An authentic Aberdeen Tunnel Bus-Bus Interchange (BBI) Passenger Information Display System (PIDS) web simulator powered by the Citybus Open Data API via DATA.GOV.HK.

---

## 🔗 線上體驗 / Live Demo

立即在瀏覽器體驗模擬器：  
👉 **[https://kenyip0244.github.io/Citybus-ATBBI-PIDS-Simulator/](https://kenyip0244.github.io/Citybus-ATBBI-PIDS-Simulator/)**

---

## 🌟 核心功能 / Features

* **真實還原介面 (Authentic Visual Design)**:
  * 完美重現城巴經典的 2×4 網格排版、藍白漸層底色與對角圓角設計。
  * 採用 Google Fonts 的 **Roboto** 專業字體顯示路線編號與抵達分鐘。
  * 依路線性質自動切換配色：市區線（藍底白字）、過海線（紅底白字）、通宵線（黑底黃字）。
* **實時數據整合 (Real-Time ETA Integration)**:
  * 自動連接城巴官方開放 API 抓取實時到站數據。
  * 支援實時 GPS 訊號圖示（以 -45 度向左上方發射顯示，限 20 分鐘以內班次）。
  * 支援「即將抵達 (Arriving)」特殊動態顯示。
* **智慧尋址與快取加速 (Smart Stop Finder & Local Caching)**:
  * 自動判斷方向並搜尋對應的香港仔隧道月台站位。
  * 整合 `localStorage` 本地快取技術，首次載入後即可實現秒速開啟。
* **全平台響應與縮放 (16:9 Auto Aspect Ratio Scaling)**:
  * 內建基於 Container Queries (`cqw`) 的等比例縮放引擎，鎖定 16:9 比例並支援全螢幕顯示。
* **全方向與月台支援 (Full Platform Coverage)**:
  * 北行（往港島北及九龍）：月台 A、B、C
  * 南行（往港島南）：月台 A、B、C

---

## 🛠️ 技術架構 / Built With

* **HTML5**
* **CSS3** (CSS Grid, Flexbox, Container Queries `cqw`, SVG Icons)
* **JavaScript (Vanilla ES6+)** (Fetch API, LocalStorage, Async/Await)
* **Data Source**: [DATA.GOV.HK Citybus Open API](https://data.gov.hk/)

---

## 🚀 快速開始 / Getting Started

### 本地運行 / Local Setup
1. 複製此儲存庫 (Clone this repository):
   ```bash
   git clone [https://github.com/kenyip0244/Citybus-ATBBI-PIDS-Simulator.git](https://github.com/kenyip0244/Citybus-ATBBI-PIDS-Simulator.git)

   ```

2. 直接在瀏覽器中開啟 `index.html` 即可運行。
*(Simply open `index.html` in any modern web browser.)*

### 部署至 GitHub Pages / Deploy to GitHub Pages

1. 將專案推送至 GitHub 儲存庫。
2. 進入儲存庫的 **Settings** -> **Pages**。
3. 在 **Branch** 選擇 `main`（或 `master`）並點擊 **Save**。
4. 部署完成後即可透過 `https://kenyip0244.github.io/Citybus-ATBBI-PIDS-Simulator/` 存取。

---

## 📖 操作指南 / User Controls

| 操作 (Action) | 功能 (Function) |
| --- | --- |
| **點擊月台按鈕 (Click Platform Button)** | 進入指定方向與月台的 PIDS 畫面。 |
| **雙擊頂部標題列 (Double Click Top Header)** | 返回主選單。(Return to main platform selector.) |
| **雙擊畫面空白處 (Double Click Screen Area)** | 切換全螢幕模式。(Toggle Fullscreen mode.) |
| **點擊「清除系統快取」 (Click Clear Cache)** | 清除本機儲存的站位 ID 快取並重新載入。 |

---

## 📄 免責聲明 / Disclaimer

* 本專案僅供個人學習、研究與交通愛好者模擬用途。
* 即時巴士到站數據版權歸城巴有限公司（Citybus Limited）及香港特區政府所有。
* This project is for educational, research, and transit simulation purposes only. Real-time ETA data is provided by Citybus Limited and DATA.GOV.HK.
