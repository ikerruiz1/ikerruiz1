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
> **[Customer Inquiry Manager](https://github.com/ikerruiz1/customer-inquiry-manager)** &nbsp;·&nbsp; [Video Demo & Walkthrough](https://youtu.be/_ZljpEMZX30)
> Customer inquiry ingestion, AI triage and human-in-the-loop ticket resolution on AWS. FastAPI backend, React operations console, ECS Fargate, RDS PostgreSQL, Amazon Bedrock.

### Architectural Highlights & Engineering Depth

* **Single-Pass AI Triage:** One Bedrock `Converse` call per ticket classifies department, urgency, impact, sentiment, churn risk and the entities worth acting on, returning a Pydantic v2-validated structure plus a drafted reply. No multi-call orchestration, and no request ever waits on the model.
* **Grounding Without Retraining:** Routing precedence rules, churn-escalation triggers and service commitments are versioned per tenant and injected into the prompt, so policy changes ship as configuration instead of a retraining cycle.
* **Adversarial & Privacy Guardrails:** Amazon Bedrock Guardrails filter prompt attacks and redact PII before inference, backed by an explicit directive that detects prompt injection, escalates it to Security at maximum urgency and refuses without leaking internal configuration.
* **Deterministic SLA Engine:** The model never computes a deadline. ITIL v4 priority, first-response and resolution targets are derived in Python from the extracted urgency and impact, with a churn-risk promotion guardrail and an SLA clock that freezes while the ticket waits on the customer.
* **Burst-Proof Ingestion:** Five inbound channels (email, web form, Trustpilot, Google Reviews, Stripe) are signature-verified and queued on SQS FIFO before any inference, with a dead-letter queue and alarms; measured ingress latency sits at p95 17ms.
* **Zero-Trust Identity & Private Data Plane:** Amazon Cognito with mandatory RFC 6238 TOTP MFA and group-based RBAC fronts a PostgreSQL database isolated in private subnets, reachable only through PrivateLink, with no public endpoint and no NAT gateways.
* **AWS-Native Delivery Pipeline:** CodePipeline, CodeBuild and CodeDeploy gate every change behind 91 automated tests, Semgrep SAST and Trivy CVE scanning, plus OPA/Conftest policy-as-code and a Syft SBOM, in a roughly 7-minute zero-downtime release.

---

## 📬 Contact & Collaboration

> [!TIP]
> Reach out if you want to talk about cloud infrastructure, DevOps, or system automation.
