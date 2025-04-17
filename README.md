# 📘 AWS 架構學習筆記

---

## 🧭 一、核心管理架構（Account & 身份管理）

- **Organizations**：多帳號統一管理、成本中心劃分  
- **IAM / SSO**：最小權限原則，MFA、角色切換、使用者群組  
- **CloudTrail**：審計紀錄所有 API 行為（操作追蹤）  
- **Config**：資源合規性管理與設定追蹤  

```
IAM User/Role -> AWS API 操作 -> CloudTrail 紀錄  
Organizations -> 統一管理帳號與政策  
```

---

## 🏗️ 二、經典三層架構

- **Route 53**：域名解析，健康檢查  
- **ALB**：7層負載均衡器，支援 path-based routing  
- **EC2 + RDS**：應用與資料庫層，部署基本 Web 架構  
- **VPC + Subnet**：網段劃分，公私子網隔離  

```
使用者 -> Route 53 -> ALB -> EC2 (應用層) -> RDS (資料層)  
```

---

## ⚡ 三、高併發架構（可擴展 + 快取）

- **Route 53 + CloudFront**：DNS + CDN 提供低延遲內容發送  
- **VPC + NAT + IGW**：安全可控的網路出口策略  
- **Auto Scaling Group (ASG)**：根據負載自動擴展 EC2 數量  
- **Elastic Load Balancer (ALB)**：多 AZ 載均分流  
- **ElastiCache（DAX for DynamoDB）**：讀取快取，加速 DynamoDB 查詢  
- **S3 + CloudFront**：靜態資源快速分發  

```
使用者 -> Route 53 -> CloudFront -> ALB -> ASG 中的 EC2 -> ElastiCache / DAX  
                                
                        ↓
                     靜態內容 S3  
```

---

## 🛠️ 四、DevOps 架構（CI/CD）

- **CodeCommit**：Git 原始碼倉庫（可用 GitHub 替代）  
- **CodeBuild**：建置與測試自動化（支援 Docker）  
- **CodeDeploy**：自動部署 EC2、ECS、Lambda  
- **CodePipeline**：整合上述流程，自動化 CI/CD  
- **CloudWatch + SNS**：監控與通知部署結果  
- **Parameter Store / Secrets Manager**：敏感資訊集中管理  

```
開發者 Push Code -> CodeCommit/GitHub -> CodePipeline  
                                        ↓  
                                  CodeBuild -> 測試/建置  
                                        ↓  
                                  CodeDeploy -> 部署至 ECS/EC2  
                                        ↓  
                                 CloudWatch/SNS 監控部署狀態  
```

---

## 🧩 五、微服務 + 物價查詢架構（以 ECS 為主）

- **ECS (Fargate)**：無伺服器容器平台，支援 service auto scaling  
- **Route 53**：服務內部名稱解析  
- **ALB**：支援容器 routing（可用 path 轉導至不同微服務）  
- **DynamoDB**：NoSQL 架構適合查詢商品價格  
- **CloudWatch Logs / X-Ray**：服務健康追蹤與追蹤鏈分析  

```
使用者 -> Route 53 -> ALB -> ECS Service（多個微服務） -> DynamoDB 查詢商品資料  
                                                ↓  
                                    CloudWatch Logs / X-Ray 追蹤  
```

---

## 🪄 六、Serverless 架構

- **API Gateway + Lambda**：事件驅動，無伺服器運算架構  
- **DynamoDB / S3 / Step Functions**：組成完整應用流程  
- **EventBridge / SNS / SQS**：解耦事件觸發與通知流程  
- **SAM / CDK**：以程式碼管理 Serverless 架構  

```
使用者 -> API Gateway -> Lambda -> DynamoDB / S3 / Step Functions  
                               ↓  
                    觸發 SNS / SQS / EventBridge 事件處理  
```

---

## ☁️ 七、混合雲架構（Hybrid Cloud）

- **Direct Connect / Site-to-Site VPN**：企業內部資料中心與 AWS 私網連線  
- **Transit Gateway**：跨帳號 / VPC 統一管理  
- **Storage Gateway / Snowball**：在地儲存與大量資料搬遷  
- **Outposts**：AWS 硬體佈建於本地資料中心  

```
企業內部資料中心 <--> Direct Connect / VPN <--> AWS VPC  
                                    ↓  
                            Transit Gateway 管理多 VPC  
                                    ↓  
                         Storage Gateway / Outposts 支援本地服務  
```

---

## 🛡️ 八、資安補強架構（Security & DDoS 保護）

- **WAF（Web Application Firewall）**：保護 Web 層（如 SQL 注入、XSS）  
- **Shield / Shield Advanced**：DDoS 保護層  
- **GuardDuty / Security Hub**：威脅偵測與整合報告  
- **KMS / IAM Policy / SCP**：加密、權限與政策控管  
- **VPC Flow Logs / CloudTrail Logs**：紀錄網路與 API 存取行為  

```
使用者流量 -> WAF -> ALB  
                  ↓  
           Shield 偵測攻擊 / CloudWatch 通知  

API 呼叫 -> IAM Policy / SCP 控管權限 -> CloudTrail 審計  
```

---
