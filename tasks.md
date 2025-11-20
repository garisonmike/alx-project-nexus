# TASKS.md: Detailed Implementation Tasks

## 🚀 Phase I: Core Infrastructure & Design
* [ ] T1.1: Configure Django settings (PostgreSQL, allowed hosts, base URLs).
* [ ] T1.2: Define User, Post, Comment, and Like models with appropriate fields (e.g., `TextField` for content, `DateTimeField` for creation, Foreign Keys).
* [ ] T1.3: Implement the **Follow** model (Many-to-Many through table between User and User).
* [ ] T1.4: **ERD Complete:** Generate ERD and link it in the Google Doc (for Submission 1).
* [ ] T1.5: Set up JWT authentication integration (user login/registration mutations).

## 💻 Phase II: GraphQL API & Resolvers (Mandatory Functionality)
* [ ] T2.1: Define Graphene **Types** for all database models (UserType, PostType, CommentType).
* [ ] T2.2: Implement **Query Resolvers** for:
    * [ ] Fetching a single post by ID.
    * [ ] Fetching all posts by a specific user.
    * [ ] Fetching a user's main feed (reverse chronological order of followed users' posts).
* [ ] T2.3: Implement **Mutation Resolvers** for:
    * [ ] `createPost(content, media_url)`
    * [ ] `toggleLike(post_id)`
    * [ ] `addComment(post_id, content)`
    * [ ] `toggleFollow(user_id)`
* [ ] T2.4: **GraphQL Playground** Setup: Ensure the hosted environment exposes the Playground for testing.

## ⚡ Phase III: Scalability & Polish (Exceptional Work Score)
* [ ] T3.1: **Query Optimization:** Review main feed query for N+1 issues; apply `select_related`/`prefetch_related`.
* [ ] T3.2: **Caching:** Implement Redis for caching profile data and post like counts.
* [ ] T3.3: **Asynchronous Tasks (Celery):** Offload notification sending and complex feed ranking logic.
* [ ] T3.4: **Testing:** Write unit tests for all models and mutation resolvers.
* [ ] T3.5: **Deployment Configuration:** Finalize `Dockerfile`, `docker-compose.yml`, and collect static files.
* [ ] T3.6: **Best Practices Check:** Verify linting, security headers, and environment variable usage.

## 📝 Phase IV: Submission Documentation
* [ ] T4.1: Finalize Presentation Deck content (ERD rationale, GraphQL schema explanation, tools).
* [ ] T4.2: Record and edit Demo Video (showcasing all core mutations and optimized queries).
* [ ] T4.3: **FINAL SUBMISSIONS:** Upload all links to the portal (Repo, ERD Doc, Slides, Video, Hosted API).