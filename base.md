### 1. 强缓存和协商缓存

[浏览器缓存](https://juejin.im/post/6844903763665240072)

[扼杀 304，Cache-Control: immutable](https://www.cnblogs.com/ziyunfei/p/5642796.html)

![请求流程](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/244a7d5cf07f421ba9d4e3dbb4a27bf4~tplv-k3u1fbpfcp-zoom-1.image)


* 强缓存 - 200, from disk cache

Cache-Control(优先级高): max-age(秒)，no-cache, no-store, private, public

Expire: 绝对时间的GMT格式的时间字符串

* 协商缓存 - 304

Etag(If-None-Match)
Last-Modify(If-Modified-Since)