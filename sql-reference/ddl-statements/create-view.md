# CREATE VIEW {#create-view}

Creates a new view from a specified SELECT query. The view is a logical table that can be referenced by future queries. Views do not contain any data and do not write data. Instead, the query specified by the view runs each time you reference the view by another query.

从指定的SELECT查询创建新视图。视图是一个逻辑表，将来的查询可以引用它。视图不包含任何数据，也不写入数据。相反，每次您通过另一个查询引用视图时，视图指定的查询都会运行。

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
create or replace view db1.v1 as select x,y from tbl;
```



