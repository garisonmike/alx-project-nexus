# Database Schema (ERD quick)

## Core Models
- User  
- Post  
- Comment  
- Like  
- Follow  
- Notification  

### Index Tips
- Index posts by `created_at`
- Composite index for Follow(follower, following)

### Soft Delete
Use `is_deleted` boolean on Post + Comment with a custom manager.
