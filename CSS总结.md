# CSS 用来给信息添加样式

### CSS样式的三种使用方法
+ 行内样式 权值最高
    - 标签内用style引用
    ```
    <p style="color:red">这是内容</p>
    ```
+ 内嵌样式 权值一般
    - 在head中声明
    ```
    <style type="text/css">
        p{
            color: red;
        }
    </style>
    ```
+ 外部样式 权值最低
    - 连接文件引入
    ```
    <link rel="stylesheet" href="CSS文件.css">
    ```

### 容器的作用
+ div用于打包各种标签 划分区块
+ span打包一段文字
+ 便于选择 添加样式

### 盒模型的属性
+ margin外边距
    - auto自己选择适合位置 一般用于居中
    - 单数值 适用于四个方向的外边距
    - 双数值 上下 左右 的外边距
    - 三数值 上 左右 下 的外边距
    - 四数值 上 右 下 左 的外边距
+ padding内边距
    - 同理与外边距
    - 没有auto

### 布局与选择器
+ 更好的编写 易于修改管理
+ 选择器分为多种
    - *全选择器 权值为0
    - 标签选择器最弱 权值为1
    - 类别选择器 权值为10
    - id选择器 只能用一次 权值为100
    - 行内属性最高 权值为1000
    - 复合选择器各种选择器空格组合在一起 权值相加

### 元素浮动
+ 浮动特征
    - 元素浮动会脱离网页
    - 离开后的空位会被补全
    - 会覆盖下面的元素
    - 但是不会覆盖下面元素中的内容
+ float属性
    - 属性值为浮动方向
    - 注意：123右浮动会变成321排列
    - 浮动排列只考虑前一个元素
+ 清除浮动影响
    - overflow:auto 超出后父元素自动调整大小
    - clear:left/right/both 使用后清除浮动元素的影响

### 背景图属性
+ background-image:url(文件位置)
+ background-repeat 排列方式
    - repeat按需要平铺 最后的会被裁剪
    - round按需要平铺 不会被裁剪但是会变形
    - space空位隔开 第一个和最后一个会被固定
    - no-repeat居中不重复
    - repeat-x横向重复 纵向只有一张
+ background-position
    - 背景在容器中水平垂直方向上的位置
    - space存在时定位将被忽略

### 边框的属性
+ border
    - width宽度
    - style样式
        - dotted圆点
        - dashed虚线
        - solid实线
        - double双实线
        - groove雕刻效果
        - ridge浮雕效果
        - inset凹陷效果
        - outset突出效果
    - color颜色

### 文本属性
+ color颜色属性
+ font-family字体属性
+ font-size字号属性
+ font-weight文字粗细属性
    - normal默认
    - bold加粗
    - lighter比父级更细
    - bolder比父级更粗
    - 数字取值100~900
+ font-style文字风格
    - normal默认跟随font-family
    - italic倾斜
+ text-indent缩进像素
+ text-align对齐方式
    - start顺序跟随
    - end反向跟随
    - left向左对齐
    - right向右对齐
    - center行内居中
    - justify两侧对齐最后一行无效
    - justify-all强制全部对齐
+ line-height行高
    - normal默认
    - 数字文字倍率
    - px具体行高
    - 技巧：元素高度与行高相同可实现文字水平居中
+ text-decoration文本修饰
    - underline下划线
    - 第一个值：text-decoration-line线的位置
    - 第二个值：text-decoration-style线的风格
    - 第三个值：text-decoration-color线的颜色
    - 第四个值：text-decoration-thickness线的粗细