# TiDB django backend

This library is based on django’s mysql backend and change some logic and support features to fit TiDB.

This package is tested in python 2.7 and django 1.8 ~ 1.11

# Usage

### Install Package

clone and install

```
# git clone https://github.com/blacktear23/django_tidb.git
# cd tidb_django
# python setup.py install
```

install from pip

```
pip install django_tidb
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
* TiDB not support `CASCADE` key word when drop column or drop table

# TODO

* Python3 support test
* Django 2.x and 3.x support test
