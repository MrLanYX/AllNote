# HTML 用来载入界面的信息

### 网页文字
+ h1~h6 标题 从大到小 h1只能存在一个
+ hr 水平线
+ p 段落文字
+ i 字体倾斜
+ br 换行
+ b 加粗字体

### 列表
+ ul无序列表
    - type头部属性值
    - 为disc时 默认实心圆
    - 为circle时 空心圆
    - 为square时 实心方块
+ ol有序列表
    - 为1时 数字排序
    - 为a时 小写字母排序
    - 为A时 大写字母排序
    - 为i时 小写希腊数字排序
    - 为I时 大写希腊数字排序

### 表格
+ table申请一个表格
    - th表头 默认加粗
    - tr行标签
    - td列标签
        - colspan合并横向格子
        - rowspan合并纵向格子

### 表单
+ from标签内的input会生效
    - input表单控件
        - type属性
        - 属性值为text 文本框
        - 属性值为password 密码框
        - 属性值为submit 提交按钮
        - 属性值为reset 重置按钮
    - method提交数据
        - post提交数据 请求会显示在地址栏上
        ```
        <form action="https://www.baidu.com" method="POST">
            <input type="text" name="loginname">
            <input type="password" name="pwd">
            <input type="submit">
        </form>
        ```
        - get获取数据 会以更加隐秘的方式提交
        ```
        <form action="https://www.baidu.com" method="GET">
            <input type="text" name="loginname">
            <input type="password" name="pwd">
            <input type="submit">
        </form>
        ```
        - get不能提交大量数据

### 图片
+ img图片标签
    - scr索引图片位置
    - alt文件加载失败显示文字

### 超链接
+ a超链接标签
    - href地址
    - target="_blank"新页面打开

### 特殊标记
+ del添加删除线
+ u添加下划线
+ sup文字变成上标