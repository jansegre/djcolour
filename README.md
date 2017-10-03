djcolour
========

Automatically use `colour.Color` in Python, `django.db.models.CharField` on the database, and `<input type="color">` on the forms.


Usage
-----

Add `djcolour` to your installed apps:

```python
INSTALLED_APPS = [
    ...
    'djcolour',
    ...
]
```

Use `ColorField` on your models:

```python
from djcolor import ColorField


class MyModel(models.Model):
    a_color = ColorField() # defaults to max_length=7
    b_color = ColorField(max_length=20) # be careful not to set it to less than 7
```

TODO
----

- [ ] Support other db backends, like IntegerField
- [ ] Support alpha channel
- [ ] Use a polyfill or dedicated widget for color picking instead of relying on `<input type="color">`
- [ ] Tests


Contributing
------------

PRs and issues are very welcome.
