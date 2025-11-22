# Async (short)

Django supports async views but use them only for I/O tasks.

Avoid mixing async views with heavy ORM operations — Django ORM is still sync.

Use async for:
- websockets
- external API calls
- long-polling
