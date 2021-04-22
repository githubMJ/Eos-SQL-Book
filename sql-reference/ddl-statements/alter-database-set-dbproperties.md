# ALTER DATABASE SET DBPROPERTIES {#alter-database-set-dbproperties}

Creates one or more properties for a database.

增加一个或更多属性给数据库。

## Synopsis\(文法\) {#synopsis}

```
ALTER (DATABASE) database_name
  SET DBPROPERTIES ('property_name'='property_value' [, ...] );
```

### Parameters\(参数\) {#parameters}

**SET DBPROPERTIES \('property\_name'='property\_value' \[, ...\]**

Specifies a property or properties for the database named`property_name`and establishes the value for each of the properties respectively as`property_value`. If`property_name`already exists, the old value is overwritten with`property_value`.

为数据库增加一个属性或者修改某个属性，如果属性相同会覆盖。

## Examples

```
ALTER TABLE table_name SET TBLPROPERTIES('creator' = 'tester');
```



