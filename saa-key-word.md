# 🧠 AWS SAA 題目關鍵字整理表（附圖示）

---

## 📊 資料處理與分析

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 🧪 **AWS Glue** | ETL、Serverless、Data Catalog | 抽取轉換載入（ETL）服務 |
| 🔍 **Amazon Athena** | Serverless SQL、S3 查詢 | 對 S3 上資料進行 SQL 查詢 |
| 🧱 **Amazon Redshift** | DWH、OLAP | 資料倉儲，支援大型分析查詢 |
| 🔎 **Amazon OpenSearch** | 搜尋、Log 分析、Dashboard | 建立搜尋與日誌分析平台 |
| 📈 **Amazon QuickSight** | BI、可視化 | 互動式數據視覺化工具 |
| 🔄 **Kinesis** | Streaming、即時處理 | 即時資料流處理與分析 |

---

## 🤖 AI / ML 相關服務

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 🧠 **SageMaker** | 機器學習、Train/Deploy | 建立、訓練與部署 ML 模型 |
| 👁 **Rekognition** | 圖像辨識、臉部偵測 | 圖像與影片分析服務 |
| 🎤 **Transcribe** | 語音轉文字 | 語音自動辨識轉錄 |
| 🗣 **Polly** | 文字轉語音 | TTS 服務，將文字變語音 |
| 💬 **Lex** | Chatbot、語音對話 | 構建對話機器人應用 |

---

## 💾 儲存與傳輸服務

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 📦 **S3** | 物件儲存、版本控管 | 廣泛應用的儲存服務 |
| 💽 **EBS (gp2/gp3)** | IOPS、Volume | EC2 的區塊儲存 |
| 🗂 **EFS** | NFS、POSIX、共用檔案系統 | 多 EC2 間共享儲存 |
| 📬 **Snowcone/Snowball** | 離線傳輸、資料遷移 | 大量資料傳輸設備 |
| 🔁 **DataSync** | 線上同步、資料轉移 | 高效線上資料遷移工具 |

---

## ⚙️ 運算與應用部署

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 💻 **EC2** | 虛擬機、手動管理 | 可自訂的 VM |
| 📦 **Fargate** | Container、無伺服器 | 無需管理基礎架構的容器服務 |
| 🌱 **Elastic Beanstalk** | 自動部署、可擴展 | 快速部署 Web 應用平台 |
| 🧬 **Lambda** | 無伺服器、事件觸發 | 執行短期程式邏輯，按次計費 |

---

## 🌐 網路與路由

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 🌐 **VPC** | 私有網路、子網路 | 定義 AWS 網路架構 |
| 🚪 **NAT Gateway** | 私網出網、彈性 IP | Private Subnet 對外通訊 |
| 🔁 **ALB / NLB** | Web 流量、TCP、負載平衡 | 負載均衡流量至多個目標 |
| 🔌 **API Gateway** | REST API、Lambda Proxy | 管理與發佈 API 服務 |
| 🌍 **Global Accelerator** | 靜態 IP、UDP 支援 | 跨區域連線最佳化 |
| 📡 **Route 53** | DNS、Failover、Geo Routing | 高可用性的 DNS 與容錯方案 |

---

## 🔐 安全性與權限控管

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|----------|--------|
| 🧑‍💼 **IAM / Role / Policy** | 權限管理、最小權限原則 | 控制誰能存取什麼資源 |
| 🏛 **SCP (Service Control Policy)** | 限制 OU、組織控制 | 控制整個 Org 可使用資源 |
| 🔐 **KMS** | 加密、金鑰管理 | 控制金鑰以保護資料 |
| 🚫 **S3 Block Public Access** | 防止資料外洩 | 封鎖 S3 公開權限設定 |
| 📜 **CloudTrail** | API 追蹤、稽核記錄 | 紀錄誰對哪些資源做了什麼 |
| 🧾 **Config** | Resource Change Tracking | 監控資源配置變化 |
| 🧙 **GuardDuty** | 威脅偵測、異常行為 | 偵測潛在的安全威脅 |
| 🦠 **Inspector** | 安全漏洞掃描 | 自動分析 EC2 容器弱點 |
| 🛡 **WAF / Shield** | Web 安全防護、DDoS | 保護 Web App 與防禦攻擊 |

---

## ⚡ 加速器服務

服務 | 🔑 關鍵字 | 🚀 用途
------|-----------|---------
🌍 Global Accelerator | 跨區連線、UDP、靜態 IP、健康檢查 | 加速全球使用者連線至最近邊緣位置，強化跨區通訊效率與容錯
🌐 CloudFront | CDN、內容快取、全球傳遞、OAI、WAF 整合 | 快取與分發靜態/動態內容，加快網站/影片等存取速度
🛣 API Gateway Caching | API 快取、流量限制、金鑰驗證 | 減少 API 呼叫延遲與重複查詢負載，提升回應效能
🚚 S3 Transfer Acceleration | 跨區上傳加速、邊緣節點、TCP 最佳化 | 使用就近的 AWS 邊緣節點，加快將大型檔案上傳至 S3
💾 ElastiCache (Redis / Memcached) | 快取層、Redis / Memcached | 快取頻繁查詢資料，減少對資料庫壓力，適合 API、Session 等應用
📈 DAX (DynamoDB Accelerator) | DynamoDB 專用快取、讀取加速 | 為 DynamoDB 查詢提供 ms 級回應速度，適合高頻查詢場景

---

## 🔍 監控 & 消息服務

服務 | 🔑 關鍵字 | 🚀 用途
------|-----------|---------
📈 CloudWatch | 指標監控、日誌紀錄、警示通知、Dashboards | 收集與視覺化各項 AWS 資源的運行狀況，主動發送警示
📬 SNS (Simple Notification Service) | 發布/訂閱模式、跨平台通知、簡訊/Email | 將警示或訊息廣播發送給多個接收者（如簡訊、Email、Lambda）
📩 SQS (Simple Queue Service) | 非同步佇列、解耦、可擴展 | 建立訊息佇列緩衝處理流程，常用於微服務之間的通訊
📌 EventBridge (原 CloudWatch Events) | 事件驅動、自動觸發、SaaS 整合 | 根據事件規則觸發其他 AWS 服務（如 Lambda），支援跨帳號事件整合
🛡 CloudTrail | 誰做了什麼、API 記錄、合規稽核 | 記錄所有 API 呼叫操作紀錄，用於稽核、資安與追蹤變更行為
🔍 AWS Config | 資源變更追蹤、合規檢查、歷史紀錄 | 記錄資源配置變化，並與預設合規規則比對（如禁止公開 S3）
📌 Amazon MQ | 傳統佇列中介（支援 AMQP、MQTT 等） | 遷移自架佇列系統如 RabbitMQ 的首選，支援企業應用整合
🛠 X-Ray | 追蹤請求流程、分析延遲瓶頸、微服務追蹤 | 視覺化分析應用中各元件處理時間，找出效能問題

---

## 🗄️ 資料庫服務  

| 服務 | 🔑 關鍵字 | 🚀 用途 |
|------|-----------|---------|
| 🐘 **RDS** | 多種引擎、Multi-AZ、備援 | 管理型關聯式資料庫（MySQL / Postgres / MariaDB 等） |
| 🌪️ **Aurora** | 高可用、自動擴展、Aurora Cluster | RDS 強化版，支援 MySQL / PostgreSQL，適合大規模應用 |
| ⚙️ **DynamoDB** | NoSQL、Serverless、Auto Scaling | 快速的 Key-Value 資料庫，無需管理伺服器 |
| 🧠 **ElastiCache** | Redis / Memcached、記憶體快取 | 提升資料庫查詢效能，加速應用存取 |
| 🔁 **DMS** | 資料遷移、異質/同質、低中斷 | 支援資料庫遷移至 AWS（包含資料複製同步） |
| 🧬 **Neptune** | 圖形資料庫、關聯網絡分析 | 適用於社交網路、推薦系統等圖形關係查詢 |
| 📚 **DocumentDB** | 相容 MongoDB、文件資料庫 | 適合儲存 JSON 類型資料，與 MongoDB 類似 |

---

## 📦 資料遷移服務比較表

| 服務 | 🔑 關鍵字 | 🚀 用途 | 🌐 網路類型 | 📊 資料類型 | 💡 使用場景 |
|------|----------|---------|--------------|--------------|--------------|
| ❄ **Snowcone / Snowball** | 離線傳輸、大量資料 | 實體設備搬資料到 AWS | **Offline（離線）** | Object / File（不限格式） | 巨量資料、無穩定網路 |
| 🔁 **DataSync** | 線上同步、快速傳輸 | 線上從本地或其他 AWS 匯入資料 | **Online（線上）** | File-based（NFS/SMB/S3） | 線上檔案伺服器同步 |
| 🛠 **DMS** | DB 遷移、跨平台支援、低中斷 | **資料庫層級**的同步與轉移 | **Online（線上）** | **資料表 / 結構化資料（SQL）** | DB 遷移（MySQL→Aurora） |

### ✅ 選用建議

| 如果你想... | 適合的服務 |
|-------------|-------------|
| 🚚 搬很多 TB 資料但沒有網路 | ❄ Snowball / Snowcone |
| 🔁 線上同步 NAS 或 SMB Server 上的檔案 | 🔁 DataSync |
| 🔄 將 MySQL / Oracle 等資料庫搬到 AWS 上（幾乎不中斷） | 🛠 DMS |
