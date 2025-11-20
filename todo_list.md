# 2. `TODO_LIST.md` (High-Level Weekly Goals)

This provides a high-level, time-bound view of the project for tracking progress.

```markdown
# TODO_LIST.md: Project Nexus - Social Media Feed

## 🗓 Week 1: Design & Setup (Nov 10 - Nov 17)
* [X] Finalize project choice: Social Media Feed Backend (GraphQL).
* [X] Initialize Git repository and set up initial Django project structure.
* [X] Define core database models (User, Post, Comment, Like, Follow).
* [X] **CREATE and SUBMIT Mandatory Deliverable 1 (ERD).**
* [ ] Set up basic User Authentication (JWT-based).

## 🗓 Week 2: Core API Development (Nov 18 - Nov 24)
* [ ] Integrate Graphene-Django.
* [ ] Create Graphene **Schema, Types, and Query Resolvers** for Post and Comment retrieval.
* [ ] Implement **Mutation Resolvers** for creating/deleting Posts and Interactions (Like/Comment).
* [ ] **SUBMIT Mandatory Deliverable 0 (GitHub Repo URL) and ensure clear README.**
* [ ] Integrate GraphQL Playground and test basic queries.

## 🗓 Week 3: Optimization & Submission Preparation (Nov 25 - Dec 1)
* [ ] Implement Asynchronous tasks (Celery/RabbitMQ) for notification and feed computation.
* [ ] Integrate Redis for caching user profiles and trending topics.
* [ ] Write comprehensive Unit/Integration Tests.
* [ ] Configure **Docker** and write deployment scripts.
* [ ] **SUBMIT Mandatory Deliverable 4 (Hosted API).**
* [ ] Prepare and **SUBMIT Mandatory Deliverable 2 (Presentation Deck).**
* [ ] Record and **SUBMIT Mandatory Deliverable 3 (Demo Video).**
* [ ] Schedule Manual QA Review (Mandatory Task 5).