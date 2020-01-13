ESlint
===

## 排除檔案或或特定語句的方法

排除特定檔案可以在根目錄建立一份eslintignore檔案，來排除特定文件或目錄。或是在整份文件的開頭加上下方語法來做排除。  
```
/* eslint-disable */
```  

要排除特定的語句可以將要排除的語句放入下方區塊內來做排除。
```
/* eslint-disable */

console.log(err.response)

/* eslint-enable */
```
> 也可以針對特定的規則做排除
```
/* eslint-disable no-console */

console.log(err.response)

/* eslint-enable */
```
