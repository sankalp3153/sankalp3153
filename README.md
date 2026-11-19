<div align="center">

<img src="./assets/hero-terminal.svg" alt="Sankalp Dev — Backend & Distributed Systems Engineer" width="100%" />

<br/>

<p align="center">
  <a href="https://www.linkedin.com/in/sankalp-dev-1918a424b/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Sankalp_Dev-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:thakursankalp974@gmail.com">
    <img src="https://img.shields.io/badge/Email-thakursankalp974%40gmail.com-15803D?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=sankalp3153&label=VIEWS&color=1E293B&style=for-the-badge" alt="Profile Views" />
</p>

</div>

---

### About Me

I'm a **Backend & Distributed Systems Engineer** currently building multi-tenant **RCS Business Messaging (RBM)** & **WhatsApp Business API** infrastructure at **Lemin AI**, and previously **Co-Founder at Coders Crux**.

My day-to-day work focuses on:
- **Event-Driven Messaging Pipelines:** Designing asynchronous producer/consumer architectures with **Apache Kafka**, Dead-Letter Queues (DLQ), exponential backoff retries, and idempotent webhook ingestion.
- **Concurrency-Safe Backend Services:** Writing low-latency APIs in **Python (FastAPI, Django, Flask)** and **Node.js (Express)** backed by **PostgreSQL** (`FOR UPDATE` locking, composite indexing) and **Redis** (sliding-window rate limiting & caching).
- **Cloud & DevOps Reliability:** Containerizing services with **Docker**, orchestrating workloads on **Kubernetes (HPA & ServiceMonitors)**, configuring **Nginx**, and automating builds via **GitHub Actions** on **AWS**.

---

### Featured Backend & Infrastructure Projects

| Repository | Architecture & Engineering Focus | Core Stack |
| :--- | :--- | :--- |
| [**`pulse-mq`**](https://github.com/sankalp3153/pulse-mq) | Event-driven messaging & webhook dispatch gateway featuring atomic Redis Lua token-bucket rate limiting, constant-time HMAC-SHA256 webhook verification, RCS→WhatsApp failover, and Kafka DLQ retries. | `Python` `FastAPI` `Kafka` `Redis` `K8s` |
| [**`ledger-core`**](https://github.com/sankalp3153/ledger-core) | Concurrency-safe multi-tenant prepaid wallet & two-phase reservation ledger (`reserve → settle / release`) using integer minor units, idempotency keys, and PostgreSQL `SELECT ... FOR UPDATE` row locking. | `Node.js` `JavaScript` `PostgreSQL` `Redis` `Docker` |
| [**`stream-guard`**](https://github.com/sankalp3153/stream-guard) | Lightweight Prometheus exposition exporter & SLA lag evaluator for Kafka consumer groups with cooldown alert deduplication and Kubernetes `ServiceMonitor` manifests. | `Python` `Kafka` `Prometheus` `Kubernetes` |
| [**`DSA`**](https://github.com/sankalp3153/DSA) | Tested distributed systems primitives (`ConsistentHashRing`, `TokenBucketLimiter`, `LRUCache`) alongside core graph, DP, and sliding-window algorithms with CI test suites. | `Python` `JavaScript` `GitHub Actions` |
| [**`crx_db`**](https://github.com/sankalp3153/crx_db) | Normalized PostgreSQL relational schema, ERD documentation, and query design powering Coders Crux hackathons, quizzes, and submissions. | `PostgreSQL` `SQL` `Schema Design` |
| [**`Chat_Analysis`**](https://github.com/sankalp3153/Chat_Analysis) | Messaging log parser and NLP analytics pipeline extracting user engagement patterns, temporal heatmaps, and content telemetry. | `Python` `NLP` `Data Analytics` |

---

### Systems Architecture Pattern

```mermaid
flowchart LR
    Client["Client SDK / Webhooks"] --> Nginx["Nginx / API Gateway"]
    Nginx --> RL["Redis Rate Limiter<br/>(Lua Token Bucket)"]
    Nginx --> Kafka[("Apache Kafka<br/>Partitioned Topics")]
    Kafka --> Workers["Async Consumer Workers<br/>(Python / Node.js)"]
    Workers --> Ledger[("PostgreSQL<br/>ACID Ledger")]
    Workers -->|Transient 429/5xx| DLQ[("Retry / DLQ Topic")]
    Workers --> Metrics["Prometheus / StreamGuard"]
```

---

### Technical Stack

<div align="center">

| Domain | Technologies |
| :--- | :--- |
| **Languages & Runtimes** | ![Python](https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=3776AB) ![JavaScript](https://img.shields.io/badge/JavaScript_ES6+-0D1117?style=flat-square&logo=javascript&logoColor=F7DF1E) ![Node.js](https://img.shields.io/badge/Node.js-0D1117?style=flat-square&logo=nodedotjs&logoColor=339933) ![Bash](https://img.shields.io/badge/Bash_/_Shell-0D1117?style=flat-square&logo=gnubash&logoColor=4EAA25) ![SQL](https://img.shields.io/badge/SQL-0D1117?style=flat-square&logo=postgresql&logoColor=4169E1) |
| **Backend & APIs** | ![FastAPI](https://img.shields.io/badge/FastAPI-0D1117?style=flat-square&logo=fastapi&logoColor=009688) ![Django](https://img.shields.io/badge/Django_REST-0D1117?style=flat-square&logo=django&logoColor=092E20) ![Flask](https://img.shields.io/badge/Flask-0D1117?style=flat-square&logo=flask&logoColor=white) ![Express](https://img.shields.io/badge/Express.js-0D1117?style=flat-square&logo=express&logoColor=white) ![WebSockets](https://img.shields.io/badge/REST_%26_Webhooks-0D1117?style=flat-square&logo=socketdotio&logoColor=white) |
| **Streaming & Data** | ![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-0D1117?style=flat-square&logo=apachekafka&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-0D1117?style=flat-square&logo=redis&logoColor=DC382D) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=4169E1) ![MySQL](https://img.shields.io/badge/MySQL-0D1117?style=flat-square&logo=mysql&logoColor=4479A1) ![MongoDB](https://img.shields.io/badge/MongoDB-0D1117?style=flat-square&logo=mongodb&logoColor=47A248) ![Celery](https://img.shields.io/badge/Celery-0D1117?style=flat-square&logo=celery&logoColor=37814A) |
| **Cloud & DevOps** | ![AWS](https://img.shields.io/badge/AWS-0D1117?style=flat-square&logo=amazonwebservices&logoColor=FF9900) ![Kubernetes](https://img.shields.io/badge/Kubernetes-0D1117?style=flat-square&logo=kubernetes&logoColor=326CE5) ![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED) ![Nginx](https://img.shields.io/badge/Nginx-0D1117?style=flat-square&logo=nginx&logoColor=009639) ![Prometheus](https://img.shields.io/badge/Prometheus-0D1117?style=flat-square&logo=prometheus&logoColor=E6522C) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-0D1117?style=flat-square&logo=githubactions&logoColor=2088FF) ![Linux](https://img.shields.io/badge/Linux-0D1117?style=flat-square&logo=linux&logoColor=FCC624) |

<br/>

<img src="https://skillicons.dev/icons?i=py,js,nodejs,fastapi,django,flask,express,kafka,redis,postgres,mysql,mongodb,aws,kubernetes,docker,nginx,linux,githubactions&perline=9" alt="Tech Stack Icons" />

</div>

---

### GitHub Activity

<div align="center">

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=sankalp3153&theme=tokyonight&hide_border=true&background=0D1015&ring=22C55E&fire=4ADE80&currStreakLabel=22C55E" width="39%" alt="GitHub Streak" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=sankalp3153&theme=github_dark" width="30%" alt="GitHub Stats" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=sankalp3153&theme=github_dark&exclude=Java,TypeScript,C,C++,CSS,HTML" width="29%" alt="Top Languages" />
</p>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=sankalp3153&theme=tokyo-night&hide_border=true&bg_color=0D1015&color=94A3B8&line=22C55E&point=4ADE80&area=true" width="100%" alt="Contribution Activity Graph" />

</div>
