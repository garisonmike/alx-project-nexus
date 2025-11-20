# PLAN.md: Social Media Feed Backend (GraphQL)

## 1. Project Goal & Technology Stack
**Goal:** Develop a highly scalable, functional backend for a social media feed, emphasizing efficient data fetching and interaction management.
**Target API:** GraphQL (using Django and Graphene) for flexible querying.
**Timeline:** November 10, 2025 - December 1, 2025 (Submission Deadline).

## 2. Architectural Design Strategy

### 2.1. Data Modeling Philosophy
We will prioritize **3rd Normal Form (3NF)** for write efficiency and data integrity. For high-read, denormalized data (like a user's primary feed), we will explore materialized views or dedicated caching layers in the optimization phase to maintain high performance.

### 2.2. Technology Stack & Environment
| Component | Technology | Rationale |
| :--- | :--- | :--- |
| **Backend Core** | Django 5.x | Robust, secure, and familiar framework for rapid development. |
| **Database** | PostgreSQL | Reliability, advanced features (JSONB, indexing), and scalability. |
| **API Layer** | Graphene-Django | Enables powerful, flexible GraphQL queries and minimizes over-fetching. |
| **Task Queue** | Celery + RabbitMQ | For asynchronous tasks (e.g., notification generation, feed pre-computation). |
| **Caching** | Redis | High-speed, in-memory caching for frequently accessed data (e.g., post counts, trending topics). |
| **Deployment** | Docker & Render/Railway | Ensures consistent, containerized environment and easy deployment. |

### 2.3. Workflow Strategy (Git & CI/CD)
1.  **Version Control:** Use Gitflow methodology (main, develop, feature branches).
2.  **Commit Convention:** Enforce conventional commits (`feat:`, `fix:`, `perf:`, `docs:`) for clear history.
3.  **CI/CD:** Integrate GitHub Actions for automated unit testing, linting (Black, Flake8), and security scans on every push to the `develop` branch.

## 3. Mandatory Deliverable Roadmap
The project will be executed in phases, ensuring all mentor submission requirements are met on time.

| Phase | Duration | Primary Focus | Mandatory Deliverable |
| :--- | :--- | :--- | :--- |
| **I: Design** | Nov 10 - Nov 17 | Database Design & Authentication setup. | **1. API Database Design (ERD)** |
| **II: Core API** | Nov 18 - Nov 24 | Post/Interaction models, Graphene integration, initial query resolvers. | **0. GitHub Repo URL & README** |
| **III: Optimization & Polish** | Nov 25 - Nov 29 | Asynchronous tasks, caching, code cleanup, final security checks. | **4. Hosted API** |
| **IV: Submission Prep** | Nov 30 - Dec 1 | Create presentation materials and video. | **2. Presentation Deck** & **3. Demo Video** |

## 4. Scalability and Optimization Considerations
* **Feed Generation:** Use Celery to asynchronously pre-compute personalized feeds or reverse-chronological feeds to avoid high-latency, runtime database lookups.
* **Interaction Counters:** Use atomic operations in PostgreSQL or cached values in Redis for counting likes/comments to handle high write volumes without contention.
* **N+1 Optimization:** Utilize Django's `select_related` and `prefetch_related` within Graphene resolvers to minimize database queries.

---