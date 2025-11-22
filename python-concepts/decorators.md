# Decorators (short)

Used everywhere in Django: views, permissions, caching.

Example: rate-limiting, permission checking, logging.

```py
def require_auth(fn):
    def wrapper(request, *args, **kwargs):
        if not request.user.is_authenticated:
            raise PermissionDenied
        return fn(request, *args, **kwargs)
    return wrapper
```
