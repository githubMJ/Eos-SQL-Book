# SHOW TABLES {#show-tables}

Lists all the base tables and views in a database.

列出数据库中的所有基表和视图。

## Synopsis\(文法\) {#synopsis}

```
SHOW TABLES [IN database_name] ['regular_expression']
```

### Parameters\(参数\) {#parameters}

**\[IN database\_name\]**

Specifies the`database_name`from which tables will be listed. If omitted, the database from the current context is assumed.

指定将从中列出表的数据库名称。如果省略，则假定当前上下文中的数据库。

**\['regular\_expression'\]**

Filters the list of tables to those that match the`regular_expression`you specify. Only the wildcard`*`, which indicates any character, or`|`, which indicates a choice between characters, can be used.

将表列表筛选为与指定的常规表达式匹配的表。只能使用表示任意字符的通配符\*，或表示字符之间。

## Examples {#examples}

```
SHOW TABLES IN sampledb;
```

## Result

```
alb_logs
cloudfront_logs
elb_logs
flights_2016
flights_parquet
view_2016_flights_dfw
```

## Examples {#examples}

```
SHOW TABLES IN sampledb '*flights*';
```

## Result

```
flights_2016
flights_parquet
view_2016_flights_dfw
```



