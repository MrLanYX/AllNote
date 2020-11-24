### 三大系列：
offset
client
scroll

+ 立即执行函数方式
    - (function(){})()
        - 注意若有两个立即执行函数连在一起，则需要用;号进行分割。
        - 所以才会出现一些执行函数的最前面有一个;号
    - (function(){}())
    - 作用：创建一个独立的作用域，可以避免命名冲突

+ offset 动态获取元素的[偏移量]
    - .offsetParent 返回元素带有[定位]的父元素
    - .offsetTop 元素距离带有[定位]的父元素顶部的距离
    - .offsetLeft 元素距离带有[定位]的父元素左边的距离
    - .offsetWidth 元素内容（包括padding、边框、内容）的宽度
    - .offsetHeight 元素内容（包括padding、边框、内容）的高度

+ client 动态获取元素[内容的大小属性]
    - .clientLeft 获取左边框宽度
    - .clientWidth 包含width,padding,但不包含border 的宽度  [内容超出不算入]

+ scroll 动态获取元素[内容的内部偏移量与属性]
    - .scrollTop 被滚动条卷去的头部 上边框下沿至内容顶部
    - window.pageYOffset 是页面卷去的头部
    - .scrollWidth 包含width,padding,但不包含border 的宽度  [但是是真实宽度内容超出也算]
    - 拖动滚动条触发事件 onscroll

+ window.scroll(x,y) 窗口滚动某个位置

### 动画效果

+ 移动动画原理
    - 获得盒子当前位置
    - 让盒子在当前位置加上1个移动距离
    - 利用定时器不断重复这个操作
    - 加一个结束定时器的条件
    - 注意此元素需要添加定位
    - [注意]函数封装之后每次都会 var 所以用对象属性的方法替代
    - [注意]如果是按钮触发 记得每次点击事前清除上一个定时器

+ 缓动效果
    - (目标距离-当前位置)/10 就是移动速度

+ 节流阀
    - 防止动画过快
    - 申明一个值flag=true
    - 如果 为true 先改为false 再执行事件函数
    - 整个事件中的动画申请一个回调函数 将flag改为true
