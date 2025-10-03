# BookIt

> 職訓局全端班 實習作品 —— Bookit 球館通 專案

## 專案簡介

Bookit 是一個簡單預約網頁，目標是讓使用者能夠管理與預約運動場地。  
本專案為職訓局全端班的實習作品，以小型開發模式，練習從零到有的開發流程。

## 功能特色

- 使用者註冊 / 登入
- 場地列表 / 瀏覽  
- 場地預約 / 取消 / 查詢  
- 場地管理者後台介面：管理預約 / 場地  
- 平台管理者後台介面：管理預約 / 場地 / 場館 / 使用者 

## 技術棧 / 工具

以下是本專案所用的主要技術與工具：

| 類別 | 工具 / 框架 |
|---|---|
| 後端 | Laravel (PHP) |
| 前端 | Blade |
| 資料庫 | MySQL |
| API / 路由 | Laravel routing |
| 打包 / 工具 | NPM / Composer |
| 部署 / 環境 | Docker / .env 環境設定 / 伺服器配置 |

## 安裝與執行（本地開發）

以下是一個簡單的安裝與開發流程，假設你在本機開發：

1. Clone 此專案  
   git clone https://github.com/red114630/bookit.git
   cd bookit
2. 安裝後端套件
   composer install
3. 安裝前端套件
   npm install
4. 複製 .env.example 並修改環境設定
   cp .env.example .env
   # 編輯 .env，填入資料庫、信件、API 鍵等資訊
5. 產生應用程式金鑰（Laravel）
   php artisan key:generate
6. 資料庫遷移與填入初始資料
   php artisan migrate
   php artisan db:seed
7. 啟動開發伺服器 / 前端開發模式
   php artisan serve
   npm run dev
8. 在瀏覽器中開啟：http://localhost:8000 或你所設定的網址


以下是本專案的主要資料夾結構範例，供你快速瀏覽整體架構：
bookit/
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── tests/
├── .env.example
├── composer.json
├── package.json
└── README.md
你可以在這些資料夾中，找到對應的控制器 (Controllers)、模型 (Models)、視圖 (Views)、前端資源 (JS / CSS)、路由設定等。


部署（上線）
以下是簡要的部署或上線步驟，視你的環境與主機不同而異：

1. 上傳程式碼到伺服器
2. 安裝後端 / 前端相依套件
3. 設定 .env 為生產環境
4. 執行資料庫遷移（php artisan migrate --force）
5. 產生優化檔案（例如 php artisan config:cache、php artisan route:cache）
6. 啟動 / 重啟伺服器
