# 公民 3D 知識星球：所有權的物權特性

## 內容來源
以使用者上傳的《公民與社會 2》第五章第二節「所有權的物權特性」（原書第 109–115 頁）設計。教材濃縮成六個區域；題目、情境與學習反思為教學改編，非教材原文試題。

## 特色
- 真正的 3D 幾何場景：Three.js 的 Sphere、Box、Cone、Cylinder，具光照、陰影、深度遮擋、透視旋轉。
- OrbitControls：滑鼠拖曳或觸控旋轉、雙指或滾輪縮放；點擊模型使用 Raycaster 射線選取。
- 六個知識島站點，依序答對解鎖、主動式鏡頭導覽。
- 六站教學概念、案例、練習、反思；教師模式提供每站的教學流程，適用 2 節 50 分鐘課程。
- 學習歷程儲存於瀏覽器 localStorage，支援 JSON 匯出與清除。
- RWD、PWA manifest 與 service worker。

## 部署到 GitHub Pages
1. 建立公開或可啟用 Pages 的 GitHub Repository。
2. 將 `index.html`、`manifest.webmanifest`、`icon.svg`、`sw.js`、`README.md` 全部放至 Repository 根目錄。
3. Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save。
4. 開啟 GitHub Pages 網址，第一次開啟需連線載入 Three.js 模組。

## 技術與使用限制
- Three.js 與 OrbitControls 由 jsDelivr CDN 匯入，因此 **第一次開啟需有網路**；PWA 快取的是網站本體，不保證第一次下載外部模組後必可離線使用。若需完整離線，應將 Three.js 與 OrbitControls 本地化並調整 import map、預先快取。
- 直接用 `file://` 開啟時，瀏覽器對 ES modules、PWA 可能有限制。建議使用 VS Code Live Server、`python -m http.server 8000`，或直接部署 GitHub Pages。
- 學生資料僅存在各自裝置和瀏覽器中，沒有雲端同步或教師後台；可要求學生匯出 JSON 交作業。
- 本網站提供教材化的法律概念，不代替個案法律意見。原始教材中的物權移轉規則屬概念性的原則說明，個案仍需參照現行法規與例外規定。

## 檔案結構
```
civic-ownership-planet/
├── index.html             # 互動網站與真正 3D 場景
├── manifest.webmanifest   # PWA 資訊
├── sw.js                  # 本地網站快取
├── icon.svg               # 網站圖示
└── README.md              # 操作與部署說明
```
