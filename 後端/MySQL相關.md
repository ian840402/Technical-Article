# MySQL 相關

## SQL Prepared Statement

可以達到 sql 指令帶參數的功能，使用此方式帶參數，sql 會先建立 sql 語句，並且將之後帶入得值視為參數，所以可以避免 sql injection 的攻擊，以提高資訊安全。

## SQL Injection

一種資料庫攻擊，因為 sql 是字串是指令操作，因此惡意人士可以透過在 sql 語法中注入惡意字串，從而達到惡意攻擊。

## 時間相關

timestamp 型態，只要有新增修改，就會自動更新現在時間間。  
新增：DEFAULT CURRENT_TIMESTAMP  
修改：ON UPDATE CURRENT_TIMESTAMP  

## 搜尋
```
WHRER 條件 = 參數   // 完全匹配

WHERE 條件 LIKE 參數    // 模糊匹配，會搭配 % or _ 來使用
 
'%參數'     // 以參數結尾的數據
'參數%'     // 以參數開頭的數據
'%參數%'    // 含有參數的數據
'_參數_'    // 三位且中間是參數的數據  
'_參數'     // 兩位且結尾是參數的數據
'參數_'     // 兩位且開頭是參數的數據
```

## 取得最後一筆新增 ID
```
SELECT LAST_INSERT_ID()
```

## 注意事項

不要對 sql 指令跑回圈