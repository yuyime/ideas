#Referrer-Policy:Referrer的策略

## 语法
+ Referrer-Policy: no-referrer
+ Referrer-Policy: no-referrer-when-downgrade
+ Referrer-Policy: origin
+ Referrer-Policy: origin-when-cross-origin
+ Referrer-Policy: same-origin
+ Referrer-Policy: strict-origin
+ Referrer-Policy: strict-origin-when-cross-origin
+ Referrer-Policy: unsafe-url

如果值无效就是默认值。


### no-referrer
整个 Referer 首部会被移除。访问来源信息不随着请求一起发送

### no-referrer-when-downgrade （默认值）
在没有指定任何策略的情况下用户代理的默认行为。在同等安全级别的情况下，引用页面的地址会被发送(HTTPS->HTTPS)，但是在降级的情况下不会被发送 (HTTPS->HTTP)。
### origin
在任何情况下，仅发送文件的源作为引用地址。例如 http://yuyime.com/index.html 会将 http://yuyime.com/ 作为引用地址。
### origin-when-cross-origin
对于同源的请求，会发送完整的URL作为引用地址，但是对于非同源请求仅发送文件的源。
### same-origin
对于同源的请求会发送引用地址，但是对于非同源请求则不发送引用地址信息
### strict-origin
在同等安全级别的情况下，发送文件的源作为引用地址(HTTPS->HTTPS)，但是在降级的情况下不会发送 (HTTPS->HTTP)。
### strict-origin-when-cross-origin
对于同源的请求，会发送完整的URL作为引用地址；在同等安全级别的情况下，发送文件的源作为引用地址(HTTPS->HTTPS)；在降级的情况下不发送此首部 (HTTPS->HTTP)。
### unsafe-url
无论是同源请求还是非同源请求，都发送完整的 URL（移除参数信息之后）作为引用地址。（最不安全的策略了）
