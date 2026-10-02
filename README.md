# Hi there 👋, I'm Iker Ruiz

> [!NOTE]
> Cloud & DevOps Engineer specialized in designing secure, immutable, and scalable multi-account cloud architectures on AWS using advanced Infrastructure as Code (IaC) and zero-trust CI/CD pipelines.

---

## 🛠️ Tech Stack & Skills

* **AI & Machine Learning:** Amazon Bedrock (Converse API, Claude Haiku 4.5, Guardrails), in-context grounding, structured outputs with Pydantic v2, human-in-the-loop review, scikit-learn
* **Cloud Providers:** AWS (IAM, VPC, ECS Fargate, ALB, RDS PostgreSQL, S3, KMS, Lambda, Secrets Manager, Cognito, SES, SNS, SQS, EventBridge, CloudWatch, PrivateLink)
* **Infrastructure as Code (IaC):** Terraform (reusable module architecture), Conftest (OPA/Rego policy-as-code), KICS, Checkov, TFLint
* **CI/CD & Automation:** AWS CodePipeline, CodeBuild and CodeDeploy, GitLab CI, GitHub Actions (OIDC, zero static credentials), Bash
* **Containers & Orchestration:** Docker, Amazon ECS Fargate (multi-container sidecars), Kubernetes (EKS, HPA, NetworkPolicy), ArgoCD, Helm
* **Backend, Frontend & Languages:** Python (FastAPI, SQLAlchemy 2.0 async), TypeScript (React 19, strict mode), Golang, SQL
* **Observability & FinOps:** AWS X-Ray, Amazon CloudWatch (metrics, logs, alarms, Embedded Metric Format), Prometheus, Grafana, AlertManager, Fluent Bit, AWS Cost Management, k6

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
