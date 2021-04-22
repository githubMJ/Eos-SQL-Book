# CREATE VIEW AS {#create-table-as}

Creates a new table populated with the results of a SELECT query.

创建一个新表从一个茶素馨结果集

## Synopsis\(文法\) {#synopsis}

```
CREATE [ OR REPLACE ] VIEW view_name AS query
```

### Parameters\(参数\) {#parameters}

`[OR REPLACE]`

REPLACE子句允许您通过替换现有视图来更新它。

`view_name 视图名`

`query SELECT查询`

## Examples

```
CREATE OR REPLACE VIEW db1.v1 AS SELECT x,y FROM tbl;
```



