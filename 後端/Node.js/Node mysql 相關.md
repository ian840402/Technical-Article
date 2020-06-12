# Node js mysql 相關

## Boolean 值得轉換

mysql 不能存布林值，所以一般會使用 TINTINT(1) 來存布林值，1 = true, 0 = false，但從資料庫提出的時候會是 0/1 ，在資料面的呈現跟操作變得不那麼直觀，所以 mysql 提供以下方式攔截資料，並把 TINYINT(1) 的值轉為布林值。

```
connection = mysql.createConnection({
  typeCast: function (field, next) {
    if (field.type === 'TINY' && field.length === 1) {
      return (field.string() === '1'); // 1 = true, 0 = false
    } else {
      return next();
    }
  }
});
```

## inser 多筆資料

node js 的 mysql 模組提供使用兩個陣列的方式來包裝多筆資料。

```
[ [ ['資料 1'],['資料 2'] ] ]
```