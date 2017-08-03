# TiDB django backend

This library is based on django’s mysql backend and change some logic and support features to fit TiDB.

For now this package is tested in python 2.7

# Usage

### Install Package

```
# git clone http://github.com/blacktear23/tidb_django.git
# cd tidb_django
# python setup.py install
```

### Update settings.py

```python
DATABASES = {
    'default': {
        'ENGINE': 'django_tidb.tidb',
        'NAME': 'database',
        'USER': 'username',
        'PASSWORD': 'password',
        'HOST': '127.0.0.1',
        'PORT': 4000,
    }
}
```

# Different Between MySQL

* TiDB not support foreign key
* TiDB require delete index before drop column
* TiDB not support `CASCADE` key word when drop index and drop column
