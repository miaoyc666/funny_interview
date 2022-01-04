#### 1.多协程panic问题和协程嵌套recover问题  
在多协程并发环境下，我们常常会碰到以下问题，假设我们现在有2个协程，我们叫它们协程A和B。  
【问题1】如果协程A发生了panic，协程B是否会因为协程A的panic而挂掉？  
【问题2】如果协程A发生了panic，协程B是否能用recover捕获到协程A的panic？  
答案：会，不能。
- 常见错误样例：[recover](https://github.com/miaoyc666/go-mistakes/blob/main/recover/main.go)
- 一种推荐的并发处理模型：[example](https://github.com/miaoyc666/go-mistakes/blob/main/recover/run.go)