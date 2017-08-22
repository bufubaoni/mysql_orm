# Mysql to orm
py2.7

this project base pydal `requiredments`

    pydal----------the base
    pymysql--------driver

## config it
you can config file 

    DATABASE_HOST = "ip"
    DATABASE_PORT = "3306"
    DATABASE_USER_NAME = "username"
    DATABASE_PASSWORD = "password"
    SCHEMA = "schema"

## use it
if you database schema name is `test` and you have table `a` in it, and the colums are `id` and `content`
you can use it blow 

config file setting next 

    DATABASE_HOST = "ip"
    DATABASE_PORT = "3306"
    DATABASE_USER_NAME = "username"
    DATABASE_PASSWORD = "password"
    SCHEMA = "test"

codeblock is 
```python
    from dynamic_tables import DyTables
    db = DyTables().get_db()

    rows = db(db.a.id > 0).select()
    #>>> a.id,a.content
    #>>> 1,1
    #>>> 2,2

```

more about for [more](http://www.web2py.com/books/default/chapter/29/06/the-database-abstraction-layer)