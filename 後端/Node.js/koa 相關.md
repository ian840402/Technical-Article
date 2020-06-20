# koa 相關

每個 middleware 層都需要有 next 去做串接
```
return await next() === await next()    // return 可以省略
```