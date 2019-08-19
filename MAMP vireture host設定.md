MAMP virture host 設定
=======

1. 安裝MAMP
2. 設定MAMP的port，設定為一般常用的port。  (Apache:80/ Nginx:80/ MySQL:3306)
3. 開器MAMP的v-hosts設定檔
```
/Applications/MAMP/conf/apache/httpd.conf
```
4. 找到v-hosts的模組設定檔案，並把註解拿掉
```
Include Applications/MAMP/conf/apache/extra/httpd-vhosts.congf
```
5. 進入vhosts的設定檔案，加入網站路徑與DNS
```
DocumentRoot "/xxx/xxx/xxx"
ServerName xxxx.xxxx.xxxx
```
6. 設定本機的host檔案
```
/etc/hosts
```
7. 加入剛剛在v-hosts設定檔裡新增的網站DNS
```
127.0.0.1   xxxx.xxxx.xxxx
```
8. 重啟MAMP即可完成


備註：可以自行複製一份v-hosts的設定，並把第四步驟的Include位置改成自己的v-hosts設定檔，這樣之後需要新增時也會比較方便。
