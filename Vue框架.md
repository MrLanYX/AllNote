### 引用方式
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <!-- 生产环境版本，优化了尺寸和速度 -->
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>

### js使用方式
    var app = new Vue({
            el: '#app',
            data: {
                数据名：数据值
            },
            methods: {
                方法名：function(){}
            },
        })

### 基本操作
+ 修改与赋值
    - v-text 修改所对应的标签内部信息 不识别标签结构
    - v-html 修改所对应的标签内部信息 识别标签结构
    - {{ 数据名 }} 支持字符拼接和运算符

+ 触发方式
    - v-on:click="方法名" 点击触发函数
    - v-on:keyup.enter 指定按键按下触发
    - @click="方法名" 简写方法
    - 方法也可以传递形参

+ 显示与隐藏
    - v-show 修改样式的方式 适用于频繁使用
    - v-if 修改html结构的方式 适用于一次性
    - ="true" 显示
    - ="false" 隐藏
    - 能够使用表达式判断显示隐藏

+ 修改属性
    - v-bind:属性名="属性值"
    - :属性名="属性值" 简写方式
    - 属性值的判断表达式
        - flag?'bind':'' 三元表达式
        - {bind:flag} 结果同上

+ for循环数据生成列表(包含多种使用方式)
    - ```<li v-for="item in arr">内容 {{ item }} </li>```
        - 根据数组arr的个数创建同等数量的li
        - 内容会被复制
        - arr的数据内容分别替换{{ item }}
        - item可替换自己想要的名字
    - ```<li v-for="(item,index) in arr">内容</li>```
        - 相比多了索引而已
        - 使用索引{{ index }}
        - index同样可替换自己想要的名字
    - 如果arr是对象数组
    - li的个数还是根据数组长度而定
    - li中的内容{{}}不够使用那li就是空的

+ 获取表单信息
    ```
    < div id = "app" >
        < input type = " text " v-model = " message " / >
    < / div >
    var app = new Vue({
        data:{
            message:"数据"
        }
    })
    ```
    - 数据之间相互影响

### 网络应用
    <!-- 引入Axios库 -->
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>

+ 网络请求获取数据
    - axios.get("地址 ?key=value&key2=value2").then(function(response){},function(err){})
    - axios.post("地址 ,{key:value,key2:value2}).then(function(response){},function(err){})