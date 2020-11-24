### Bom比Dom大，Bom包含Dom

### Bom的组成
+ window(浏览器的顶级对象)
    - document（文档对象模型）
    - location（url相关）
    - navigation（用户浏览器相关信息）
    - screen
    - history（路由历史记录）

+ 两种页面加载
    - window.addEventListener('load', function() {})
        - 使得代码能够放在任意位置
        - 文档加载结束再执行
            - window.addEventListener('pageshow', function(e) {}) 事件
            - load与pageshow的区别
            - 浏览器的刷新，前进后退，a链接跳转都会触发onload事件
            - 但在火狐浏览器中有“往返缓存”，会将整个页面缓存在内存中，所以在前进后退的时候访问的是缓存的页面，此时不会调用onload方式
            - 解决火狐浏览器的缓存问题：使用pageshow事件，该事件会在页面显示的时候调用，不管该页面是否来自缓存。
            - 另外，在一个页面显示时，会先触发load方法，再触发pageshow方法
    - document.addEventListener('DOMContentLoaded', function() {})
        - 仅在DOM文件加载之后执行
        - 不包括样式表 图片 flash等等
        - 用于图片加载慢的网站

+ 窗口大小事件
    - window.addEventListener('resize', function() {})
    - 窗口大小改变时触发
    - 可以通过 window.innerWidth 获取屏幕宽度

+ 定时器
    - setTimeout(函数,延时时间)
        - clearTimeout(定时器名字) 清除定时器
    - setInterval(函数,循环时间)
        - 注意：重新置入新的倒计时原来的还在运行
        - clearInterval(定时器名字) 停止定时器

+ js执行机制
    - js属于单线程语言
    - 但是新的规则中允许多线程运行
    - 代码不会出现堵塞
    - 优先执行执行站中的同步任务
    - 同步执行完之后将异步任务的结果放入执行站中执行
    - 异步任务进入等待的任务队列中要经过异步处理器的允许
    - 例如遇到点击事件 它会等你点击后放入 遇到计时事件 时间到了会自动放入
    - 主线程结束后不断获取异步任务执行

+ location对象 获取解析URL
    - protocol : // host[:port] / path / [?query] #fragment
        - 通过 location.href 获取
    - protocol 通信协议
    - host 主机域名
        - 通过 location.host 获取
    - port 端口号
        - 通过 location.port 获取
    - path 路径
        - 通过 location.pathname 获取
    - query 参数
        - 通过 location.search 获取
    - fragment 片段
        - 通过 location.hash 获取
    - location.assign() 跟href一样 跳转页面 能够后退
    - location.replace() 替换当前页面 不计入历史 不能返回
    - location.reload() 重新加载页面 类似F5

+ navigator对象 包含浏览器信息
    - navigator.userAgent 用户使用的浏览器、系统等设备信息

+ history对象 包含历史记录
    - history.back() 后退
    - history.forward() 前进
    - history.go() 参数为1前进一个页面 参输为-1后退一个页面