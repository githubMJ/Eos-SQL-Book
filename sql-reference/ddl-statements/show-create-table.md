# SHOW CREATE TABLE {#show-create-table}

Analyzes an existing table named`table_name`to generate the query that created it.

展示一个存在的且命名为table\_name从而展示它的创建结构。

## Synopsis\(文法\) {#synopsis}

```
SHOW CREATE TABLE [db_name.]table_name
```

### Parameters\(参数\) {#parameters}

**TABLE  \[db\_name.\]table\_name**

The`db_name`parameter is optional. If omitted, the context defaults to the current database.

catalog 数据源  和 db\_name 数据库参数是可选的。如果省略，则上下文默认为当前数据库。



## Examples {#examples}

```
SHOW CREATE TABLE orderclickstoday;    
```

    SHOW CREATE TABLE `salesdata.orderclickstoday`;



