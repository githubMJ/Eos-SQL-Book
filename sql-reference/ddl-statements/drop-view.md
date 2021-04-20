# DROP VIEW {#drop-view}

Drops \(deletes\) an existing view. The optional`IF EXISTS`clause causes the error to be suppressed if the view does not exist.

删除现有视图。如果视图不存在，则`IF EXISTS`选项会导致错误。

## Synopsis\(文法\) {#synopsis}

```
DROP VIEW [ IF EXISTS ] view_name;
```

### Parameters\(参数\) {#parameters}

`IF EXISTS 可选 如果存在的意思。`

view\_name` 视图名`

## Examples

```
DROP VIEW orders_by_date;

DROP VIEW IF EXISTS orders_by_date;
```



