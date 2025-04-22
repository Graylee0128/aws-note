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
