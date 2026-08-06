# Hi there 👋, I'm Iker Ruiz

> [!NOTE]
> Cloud & DevOps Engineer specialized in designing secure, immutable, and scalable multi-account cloud architectures on AWS using advanced Infrastructure as Code (IaC) and zero-trust CI/CD pipelines.

---

## 🛠️ Tech Stack & Skills

* **Cloud Providers:** AWS (Amazon Security, IAM, VPC, EC2, RDS, S3, KMS, EventBridge, SNS, AWS Backup, AWS Config)
* **Infrastructure as Code (IaC):** Terraform, TFLint, Checkov, AWS CloudFormation
* **CI/CD & Automation:** GitHub Actions (OIDC token assumption, zero static credentials), Bash Scripting, Jenkins
* **Containers & Orchestration:** Docker, Kubernetes (EKS), Amazon ECS, AWS Fargate
* **Backend & Serverless:** Python, AWS Lambda, API Gateway, DynamoDB, Amazon Cognito
* **Monitoring & FinOps:** AWS Cost Management, Amazon CloudWatch, Google Gemini AI SDK

---

## 🚀 Featured Project

> [!IMPORTANT]
> **[Automated Backup System](https://github.com/ikerruiz1/automated-backup-system)**
> Centralized, and immutable disaster recovery infrastructure engineered from the ground up to guarantee strict RTO/RPO compliance and absolute ransomware resilience.

### Architectural Highlights & Engineering Depth

* **WORM-Protected Immutability:** Implements AWS Backup Vault Lock in strict Compliance Mode, enforcing architectural-level immutability that prevents accidental or malicious deletion (even by root administrators).
* **Zero-Trust GitOps Pipeline:** Fully automated deployments via GitHub Actions utilizing OpenID Connect (OIDC) federation, completely eliminating long-lived static AWS credentials and minimizing the blast radius.
* **Proactive Security Gate:** Integrates rigorous static analysis and compliance validation via **TFLint** and **Checkov** directly into the pull request pipeline to block insecure configurations before deployment.
* **Dynamic Resource Orchestration:** Uses dynamic resource tagging (`Backup = "true"`) for autonomous, account-wide backup discovery and centralized orchestration across S3, EBS, and RDS PostgreSQL instances.
* **Resilient Infrastructure Design:** Workloads reside within an isolated multi-tier VPC protected by AWS PrivateLink (VPC Endpoints) and fully encrypted using Customer Managed KMS Keys.
* **Automated Disaster Recovery & Observability:** Configured with automated weekly restore simulations, real-time alerting via Amazon EventBridge and SNS, and continuous compliance posture tracking using AWS Config.

---

## 📬 Contact & Collaboration

> [!TIP]
> Open to high-impact Cloud, DevOps, and Infrastructure engineering opportunities where automation, security, and scalability are critical business drivers. Let's build resilient systems together.
