# MySQL 相關

## SQL Prepared Statement

可以達到 sql 指令帶參數的功能，使用此方式帶參數，sql 會先建立 sql 語句，並且將之後帶入得值視為參數，所以可以避免 sql injection 的攻擊，以提高資訊安全。

## SQL Injection

一種資料庫攻擊，因為 sql 是字串是指令操作，因此惡意人士可以透過在 sql 語法中注入惡意字串，從而達到惡意攻擊。