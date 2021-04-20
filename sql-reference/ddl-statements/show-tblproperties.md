# SHOW TBLPROPERTIES {#show-tblproperties}

Lists table properties for the named table.

列出命名表的表属性。

## Synopsis\(文法\) {#synopsis}

```
SHOW TBLPROPERTIES table_name [('property_name')]
```

### Parameters\(参数\) {#parameters}

**\[\('property\_name'\)\]**

If included, only the value of the property named`property_name`is listed.

如果包含，则只列出属性name和value值。

## Examples {#examples}

```
SHOW TBLPROPERTIES tb1;
```

```
SHOW TBLPROPERTIES orders('tb1');
```



