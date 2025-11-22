# Context Managers

Used for resources like files and database transactions.

In Django, `transaction.atomic()` is the most common.

```py
from django.db import transaction

with transaction.atomic():
    # create post + metadata safely
    ...
```