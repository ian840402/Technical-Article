Javascript 陣列操作
==========================

1. 新增陣列

```
arr.push()

var arr = [1,2,3];
arr.push(4);
console.log(arr);   //輸出結果為 [1,2,3,4]
```

2. 刪除陣列值 (*陣列引索還是會存在*)

```
delete arr[];

var arr = [1,2,3]
delete arr[0];
console.log(arr);    //輸出結果為 [empty,2,3]
```

3. 刪除陣列項目

```
arr.pop()    //刪除陣列最後一個項目
arr.shift()  //刪除陣列第一個項目

var arr = [1,2,3]
arr.pop();
console.log(arr);    //輸出結果為 [1,2]
arr.shift();
console.log(arr);    //輸出結果為 [2]
```

4. 刪除陣列多個項目並刪除index，並同時可以新增多個項目

```
arr.splice(index,length,item1......item10)   //index：刪除的起始位置，length：從index開始算刪除的數量，item：新增的項目

var arr = [1,2,3];
arr.splice(0,2,four,five);
console.log(arr);    //輸出結果為 [3,four,five]
```

5. 清空陣列

```
arr = [];
arr.length = 0;   //兩種方式都可以清空陣列

var arr = [1,2,3];
arr.length = 0;
console.log(arr);    //輸出結果為 []
```

*備註：當陣列清空時，若是對此陣列做邏輯判斷，還是可以判斷的出來，因為對js來說陣列裡的東西還是存在！！！*

6. 查詢陣列中是否有值

```
arr.includes(var);  //若是陣列中有值返回true，反之返回false

var arr = [1,2,3];
arr.includes(1);  //返回true
```
