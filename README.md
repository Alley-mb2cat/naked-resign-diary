# 🌿 裸辭日記

> 透過目標、規劃與每日反思，降低裸辭路上的焦慮與不安。

一個給裸辭者的 PWA 日記應用，幫助你在裸辭的旅程中保持方向感與心理穩定。

## 功能

### 模組 A — 裸辭評估測驗
- 三個維度評估：資金面、心理面、目標面
- 9 道情境題，視覺化呈現準備程度
- 可隨時重新測驗

### 模組 B — 準備期
- **設定大目標**：最多 5 個目標，各有代表色
- **靈感庫**：每個目標底下自由新增想做的事
- **給自己的信**：寫給未來低潮時的自己

### 模組 C — 每日日記
1. 選擇今天對應的目標（或標記休息日）
2. 從靈感庫勾選完成的事 + 自由記錄
3. 小反思 — 今天有什麼特別的心得與想法？
4. 感恩日記（1～3 件事）
5. 完成後收到系統肯定句

### 模組 D — 追蹤與回顧
- **前進軌跡**：月曆視圖，用目標顏色標記有寫日記的日子
- **週回顧**：各目標推進天數、靈感完成度、週肯定句

## 技術

- 純前端 React（CDN），無需 build
- localStorage 持久化儲存
- PWA：可加到手機主畫面，支援離線
- 支援 Dark Mode

## 部署

### Netlify（推薦）
1. Fork 這個 repo
2. 到 [Netlify](https://app.netlify.com) → New site → Import from Git
3. 選擇這個 repo，Publish directory 設為 `.`
4. Deploy！

之後改版只要 `git push`，Netlify 會自動重新部署。

### 其他
- **Vercel**：Import Git repo，Framework 選 Other
- **GitHub Pages**：Settings → Pages → Source 選 main branch
- **Cloudflare Pages**：連接 repo，Build output 設為 `.`

## 安裝到手機

### iOS
Safari 打開 → 分享按鈕 → 「加入主畫面」

### Android
Chrome 打開 → 自動提示安裝，或選單 →「安裝應用程式」

## 檔案結構

```
├── index.html        # 主程式（React App + 所有元件）
├── manifest.json     # PWA manifest
├── sw.js             # Service Worker（離線快取）
├── netlify.toml      # Netlify 部署設定
├── .gitignore
└── README.md
```

## 資料儲存

所有資料存在瀏覽器 localStorage，包含：
- 目標與靈感庫
- 每日日記紀錄
- 給自己的信
- 測驗結果
- Onboarding 狀態

可在 設定 → 資料 手動清除。

---

*裸辭不是逃避，是你選擇誠實面對自己。*
