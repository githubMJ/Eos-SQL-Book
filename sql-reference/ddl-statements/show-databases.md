# SHOW DATABASES {#show-databases}

Lists all databases defined in the metastore. You can use`DATABASES`or`SCHEMAS`They mean the same thing.

列出所有在该元数据中定义的所有数据库，你可以使用DATABASES或者SCHEMAS做相同的查询。

## Synopsis\(文法\) {#synopsis}

```
SHOW {DATABASES | SCHEMAS} [LIKE 'regular_expression']
```

### Parameters\(参数\) {#parameters}

**\[LIKE '`regular_expression`'\]**

Filter out the matching database names。

过滤出匹配的数据库名称。



## Examples {#examples}

```
SHOW SCHEMAS;

SHOW DATABASES;

SHOW DATABASES LIKE '.*analytics';

SHOW SCHEMAS LIKE '.*analytics';
```



