# DROP DATABASE {#drop-database}

Removes the named database from the catalog. If the database contains tables, you must either drop the tables before running

`DROP DATABASE`or use the`CASCADE`clause. The use of`DATABASE`and`SCHEMA`are interchangeable. They mean the same thing.

删除命名数据库.如果数据库包含表，则必须在运行drop database之前删除这些表，或者使用CASCADE子句。`DATABASE`and`SCHEMA做相同的事。`

## Synopsis\(文法\) {#synopsis}

```
DROP {DATABASE | SCHEMA} [IF EXISTS] database_name [RESTRICT | CASCADE]
```

### Parameters\(参数\) {#parameters}

**\[IF EXISTS\]**

Causes the error to be suppressed if`database_name`doesn't exist.

如果名为`database_name的库不存在删除就会报错。`

**\[RESTRICT\|CASCADE\]**

**`RESTRICT：如果数据库包含表，则不会删除该数据库，如果不写默写是该模式。`**

**`CASCADE：会强制删除所有数据库表。`**

## Examples

    DROP DATABASE clickstreams;
    DROP SCHEMA clickstreams;

    DROP DATABASE `DB1` RESTRICT;
    DROP DATABASE IF EXISTS `DB1` RESTRICT;



