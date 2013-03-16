---
layout: post
title : Using static file on django
category: django
tags: [django, python]
---
{% include JB/setup %}

Adding these into the `polls/url.py`:  

```python
from django.contrib.staticfiles.urls import staticfiles_urlpatterns

urlpatterns += staticfiles_urlpatterns()
```

Adding these into the `setting.py`:

```python
import os
HERE = os.path.join(os.path.dirname(__file__), '../static/')
# Additional locations of static files
STATICFILES_DIRS = (
    HERE,
    # Put strings here, like "/home/html/static" or "C:/www/django/static".
    # Always use forward slashes, even on Windows.
    # Don't forget to use absolute paths, not relative paths.
)
```

And, the html pattern is like this below:

```html
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Bootstrap -->
    <link href="../static/css/bootstrap.min.css" rel="stylesheet" media="screen">
</head>
```

