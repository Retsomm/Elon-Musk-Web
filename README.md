# Elon Musk World (EMW)

一個介紹伊隆·馬斯克（Elon Musk）及其相關公司、新聞、書籍、影片與 Podcast 的互動式網站。

## 🚀 特色功能

- 📅 馬斯克生平大事年表互動展示
- 🏢 旗下公司詳細介紹（SpaceX、Tesla、X Corp、The Boring Company、Neuralink、Grok）
- 📰 最新新聞自動抓取與智能快取
- 📚 書籍、YouTube、Podcast 精選與個人收藏
- 👤 完整會員系統（Email/Google OAuth 註冊登入）
- 💬 互動留言板與社群功能
- 📱 響應式設計，支援各種裝置

## 🛠 技術棧

### 前端

- **React 18** + **Vite** - 現代化前端開發框架
- **Tailwind CSS** + **DaisyUI** - 原子化 CSS 框架與 UI 元件庫
- **React Router DOM** - 單頁應用路由管理
- **React Hooks** - 狀態管理與生命週期

### 後端與服務

- **Firebase Authentication** - 身份驗證服務
- **Firebase Realtime Database** - 即時資料庫
- **Firebase Hosting** - 靜態網站部署
- **Firebase Cloud Functions** - 伺服器端邏輯

### 開發工具

- **ESLint** - 程式碼品質檢查
- **PostCSS** - CSS 後處理器
- **Vite** - 快速建置工具
- **Git** - 版本控制

## 📁 完整專案架構

```
EMW-main/
├── 📁 src/                          # 主要原始碼目錄
│   ├── 📁 component/                # 可重用元件與數據
│   │   ├── 📄 Header.jsx           # 網站標頭元件
│   │   ├── 📄 Footer.jsx           # 網站頁尾元件
│   │   ├── 📄 Navigation.jsx       # 導航選單元件
│   │   ├── 📄 LoadingSpinner.jsx   # 載入動畫元件
│   │   ├── 📄 NewsCard.jsx         # 新聞卡片元件
│   │   ├── 📄 CompanyCard.jsx      # 公司介紹卡片
│   │   ├── 📄 MediaCard.jsx        # 媒體資源卡片
│   │   ├── 📄 TimelineItem.jsx     # 時間軸項目元件
│   │   ├── 📄 ProtectedRoute.jsx   # 路由保護元件
│   │   └── 📁 data/                # 靜態數據文件
│   │       ├── 📄 timeline.js      # 時間軸數據
│   │       ├── 📄 companies.js     # 公司資訊數據
│   │       ├── 📄 quotes.js        # 名言數據
│   │       ├── 📄 books.js         # 書籍數據
│   │       ├── 📄 videos.js        # 影片數據
│   │       └── 📄 podcasts.js      # Podcast 數據
│   │
│   ├── 📁 pages/                    # 主要頁面元件
│   │   ├── 📄 Home.jsx             # 首頁
│   │   ├── 📄 Timeline.jsx         # 時間軸頁面
│   │   ├── 📄 Companies.jsx        # 公司介紹頁面
│   │   ├── 📄 News.jsx             # 新聞中心頁面
│   │   ├── 📄 Media.jsx            # 媒體資源頁面
│   │   ├── 📄 Books.jsx            # 書籍頁面
│   │   ├── 📄 Videos.jsx           # 影片頁面
│   │   ├── 📄 Podcasts.jsx         # Podcast 頁面
│   │   ├── 📄 Profile.jsx          # 會員中心頁面
│   │   ├── 📄 Login.jsx            # 登入頁面
│   │   ├── 📄 Register.jsx         # 註冊頁面
│   │   ├── 📄 Messages.jsx         # 留言板頁面
│   │   └── 📄 NotFound.jsx         # 404 錯誤頁面
│   │
│   ├── 📁 contexts/                 # React Context 狀態管理
│   │   ├── 📄 AuthContext.jsx      # 身份驗證狀態
│   │   ├── 📄 ThemeContext.jsx     # 主題狀態
│   │   └── 📄 UserContext.jsx      # 用戶數據狀態
│   │
│   ├── 📁 hooks/                    # 自定義 React Hooks
│   │   ├── 📄 useAuth.js           # 身份驗證 Hook
│   │   ├── 📄 useTheme.js          # 主題切換 Hook
│   │   ├── 📄 useLocalStorage.js   # 本地儲存 Hook
│   │   ├── 📄 useNews.js           # 新聞 API Hook
│   │   └── 📄 useFirebase.js       # Firebase 操作 Hook
│   │
│   ├── 📁 api/                      # API 相關功能
│   │   ├── 📄 firebase.js          # Firebase 設定與初始化
│   │   ├── 📄 auth.js              # 身份驗證 API
│   │   ├── 📄 database.js          # 資料庫操作 API
│   │   ├── 📄 newsAPI.js           # 新聞 API 服務
│   │   └── 📄 storage.js           # 檔案儲存 API
│   │
│   ├── 📁 utils/                    # 工具函數
│   │   ├── 📄 dateUtils.js         # 日期處理工具
│   │   ├── 📄 formatUtils.js       # 格式化工具
│   │   ├── 📄 validation.js        # 表單驗證工具
│   │   └── 📄 constants.js         # 常數定義
│   │
│   ├── 📁 styles/                   # 樣式文件
│   │   ├── 📄 globals.css          # 全域樣式
│   │   ├── 📄 components.css       # 元件樣式
│   │   └── 📄 animations.css       # 動畫樣式
│   │
│   ├── 📄 App.jsx                  # 主應用程式元件
│   ├── 📄 main.jsx                 # 應用程式入口點
│   └── 📄 index.css                # 主要樣式文件
│
├── 📁 public/                       # 靜態資源目錄
│   ├── 📄 vite.svg                 # Vite 圖標
│   ├── 📄 favicon.ico              # 網站圖標
│   ├── 📁 images/                  # 圖片資源
│   │   ├── 📄 elon-musk.jpg        # 馬斯克照片
│   │   ├── 📄 spacex-logo.png      # SpaceX 標誌
│   │   ├── 📄 tesla-logo.png       # Tesla 標誌
│   │   └── ...                     # 其他圖片
│   └── 📁 icons/                   # 圖標資源
│       ├── 📄 company-icons/       # 公司圖標
│       └── 📄 social-icons/        # 社交媒體圖標
│
├── 📁 functions/                    # Firebase Cloud Functions (可選)
│   ├── 📄 index.js                 # Functions 入口點
│   ├── 📄 package.json             # Functions 依賴
│   ├── 📁 api/                     # API Functions
│   │   ├── 📄 news.js              # 新聞抓取 Function
│   │   └── 📄 notifications.js     # 通知 Function
│   └── 📁 utils/                   # Functions 工具
│
├── 📁 config/                       # 設定文件目錄
│   ├── 📄 firebase.config.js       # Firebase 設定
│   └── 📄 api.config.js            # API 設定
│
├── 📁 docs/                         # 文檔目錄
│   ├── 📄 SETUP.md                 # 安裝說明
│   ├── 📄 DEPLOYMENT.md            # 部署指南
│   └── 📄 API.md                   # API 文檔
│
├── 📄 .env.example                 # 環境變數範例
├── 📄 .env.local                   # 本地環境變數 (被 .gitignore)
├── 📄 .gitignore                   # Git 忽略檔案設定
├── 📄 .firebase.json               # Firebase 部署設定
├── 📄 .firebaserc                  # Firebase 專案設定
├── 📄 eslint.config.js             # ESLint 程式碼檢查設定
├── 📄 postcss.config.js            # PostCSS 設定
├── 📄 tailwind.config.js           # Tailwind CSS 設定
├── 📄 vite.config.js               # Vite 建置工具設定
├── 📄 package.json                 # 專案依賴與腳本
├── 📄 package-lock.json            # 依賴版本鎖定
├── 📄 index.html                   # HTML 入口模板
└── 📄 README.md                    # 專案說明文件
```

## 🏗️ 架構說明

### 前端架構

- **組件化設計**：將 UI 拆分為可重用的 React 元件
- **頁面路由**：使用 React Router 管理單頁應用路由
- **狀態管理**：使用 React Context 管理全域狀態
- **自定義 Hooks**：封裝邏輯重用，提高程式碼可維護性

### 資料流架構

```
用戶操作 → React 元件 → Custom Hooks → API 層 → Firebase → 資料回傳
```

### 主題系統架構

```
ThemeContext → useTheme Hook → localStorage → DaisyUI 主題切換
```

### 身份驗證架構

```
Firebase Auth → AuthContext → useAuth Hook → ProtectedRoute → 頁面存取控制
```
