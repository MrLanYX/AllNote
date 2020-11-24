### dom操作总汇（重点核心）

+ 创建：
    - docment.write() 文档写入
    - document.innerHTML 标签添加内容
    - document.createElement() 创建节点 配合添加节点使用

+ 增加：
    - XXX.appendChild(YYY) 给XXX的孩子末尾添加一个节点YYY
    - XXX.insertBefore(YYY,XXX.children[0]) 给XXX的孩子前面添加一个节点YYY

+ 复制克隆
    - XXX.cloneNode()
    - 括号为空 只克隆标签
    - 括号里面为true就是全拷贝

+ 删除：
    - removeChild() 例如div.removeChild(div.children[2])

+ 修改：
    - 修改元素内容:innerHTML,innerText
    - 修改元素属性:src,href,title
    - 修改表单元素：value,type,checked
    - 修改元素样式:style,className

+ 查询（获取元素）：
    - dom提供的api:getElementById、getElementsByTagName 古老方法，不推荐
    - h5提供的api:querySelector、querySelectorAll 提倡
    - 利用节点层次关系获取元素  提倡
        - 获取父节点parentNode
        - 获取子节点children
        - 获取上一个兄弟previousElementSibling
        - 获取下一兄弟nextElementSibing

+ 修改属性-自定义属性
    - setAttribute添加
    - getAttribute获取
    - removeAttribute删除

+ 添加事件操作：
    - 鼠标点击触发click
    - 鼠标经过触发[区别]
        - mouseover子元素也会触发
        - mouseenter不存在冒泡
    - 鼠标离开触发
        - mouseout离开任何一个子元素就触发
        - mouseleave离开所有子元素触发
    - 获得鼠标焦点focus
    - 失去鼠标焦点blur
    - 鼠标移动触发mousemove
    - 鼠标弹起触发mouseup
    - 鼠标按下触发mousedown