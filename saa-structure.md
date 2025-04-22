# 🌐 AWS SAA 考試架構服務速查表

依架構分類整理 AWS 常考服務關鍵字，含 ✅ Free Tier 支援、🔗常見搭配建議！

---

## ☁️ Serverless 架構

| 服務              | 關鍵字/功能            | Free Tier | 常見組合                |
|-------------------|------------------------|-----------|-------------------------|
| Lambda            | 無伺服器運算            | ✅        | API Gateway + Lambda   |
| API Gateway       | RESTful / WebSocket API | ✅        | 前端 → API GW → Lambda |
| DynamoDB          | NoSQL、低延遲、高擴展性  | ✅        | Lambda + DynamoDB      |
| Step Functions    | 工作流編排              | ✅        | Lambda + SFN           |
| EventBridge       | 事件驅動架構              | ✅        | CloudTrail + Lambda    |
| SQS / SNS         | 非同步溝通              | ✅        | Lambda + SQS/SNS       |
| AppConfig         | 配置管理                | ✅        | Lambda + AppConfig     |

---

## 🏗️ 傳統 2-tier / 3-tier 架構

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| EC2               | 虛擬伺服器                | ✅        | ALB + EC2 + RDS           |
| RDS (Single-AZ)   | 管理式 SQL 資料庫         | ✅        | Web + RDS                 |
| ALB / NLB         | 應用層 / 網路層負載平衡器  | ✅        | EC2 / ECS / Lambda        |
| Auto Scaling Group| 自動擴縮 EC2              | ✅        | ASG + ALB + EC2           |
| Security Group    | Stateful 防火牆           | ✅        | ALB ↔ SG ↔ EC2            |
| NACL              | Stateless 子網防火牆       | ✅        | 補強 VPC 流量控制         |

---

## 🔄 資料移轉與同步

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| DataSync          | 資料中心 ↔ AWS 檔案同步    | ✅        | NFS / SMB → S3 / EFS      |
| AWS Snowcone      | 實體設備資料匯入          | ❌        | 離線傳輸大量資料           |
| DMS               | SQL ↔ SQL, NoSQL 遷移     | ✅        | RDS → Aurora、MySQL等     |
| S3                | 物件儲存、版本控管         | ✅        | Source of Truth           |
| File Gateway      | 在地 → S3 存取橋接         | ✅        | On-prem NFS + S3          |

---

## 📊 資料分析與視覺化

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| Glue              | ETL 工具                 | ✅        | S3 + Glue + Athena        |
| Athena            | SQL 查詢 S3 資料          | ✅        | Glue + S3 + Athena        |
| OpenSearch        | 日誌分析、搜尋引擎        | ✅        | CloudTrail + OS          |
| QuickSight        | BI 圖表視覺化              | ❌        | Athena + QS              |
| Kinesis           | 串流處理（影片/IoT）      | ✅        | Firehose + Lambda         |

---

## 🔐 安全與稽核

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| IAM Role/Policy   | 權限授與                 | ✅        | Lambda Execution Role     |
| SCP (Org)         | 管理帳號層級限制         | ✅        | 限制 member account 設定  |
| CloudTrail        | 誰做了什麼（稽核記錄）     | ✅        | CT + S3 + Athena          |
| Config            | 資源變更追蹤（狀態比對）   | ✅        | Config + Rule             |
| GuardDuty         | 威脅偵測                 | ✅        | VPC Log + GD              |
| WAF / Shield      | Web 防火牆、DDOS 保護     | ✅        | ALB / CloudFront + WAF    |
| Inspector         | 自動掃描 CVE 漏洞        | ✅        | EC2 + Inspector           |

---

## ⚙️ CI/CD 與開發工具

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| CodeCommit        | Git 儲存庫               | ✅        | Source 管理                |
| CodeBuild         | 編譯建置工具              | ✅        | Build → Deploy             |
| CodeDeploy        | 自動部署 EC2/ECS          | ✅        | EC2 + CodeDeploy           |
| CodePipeline      | 整合流程線                | ✅        | CI/CD Pipeline 全自動化    |
| Cloud9            | 線上 IDE                  | ✅        | Dev Environment            |

---

## 🌍 全球流量與高可用性

| 服務              | 關鍵字/功能              | Free Tier | 常見組合                   |
|-------------------|--------------------------|-----------|----------------------------|
| Route 53          | DNS、Failover            | ❌        | Route53 + S3 Hosting       |
| Global Accelerator| Global TCP/UDP 加速      | ❌        | GA + ALB / EC2             |
| CloudFront        | CDN、快取、WAF 支援       | ✅        | S3 / ALB + CloudFront      |
| ELB Multi-AZ      | 負載平衡器 + 高可用性      | ✅        | ALB + Auto Scaling         |

---

## 💡 溫馨提醒

- 🔄 **DynamoDB vs RDS**：DynamoDB 是 Serverless、RDS 是有狀態 SQL。
- 🧠 **Lambda 搭配 API Gateway 處理 RESTful**，但後端運算邏輯仍需 Lambda。
- 💰 **很多服務有 Free Tier，但有流量或執行時間限制**，要小心免費額度用完！
