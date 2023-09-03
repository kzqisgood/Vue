# 构建用户界面

### 创建Vue实例，初始化渲染

核心步骤

1.准备容器

2.引包

3.创建Vue实例

4.指定配置项 ->渲染数据

- el指定挂载点
- data提供数据

```
    <div id="app">
      <h1> {{ msg }}</h1> 
      <a href="#">{{count}}</a>
    </div> 
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
    <script>
        const app= new Vue({
            el: '#app',
            data: {
                msg: 'hello world',
                count: 666
            }
        })
    </script>
```

# 插值表达式**{{}}**

是Vue的模板语法

- 1.利用表达式插值，渲染到页面中

表达式:是可以被求值的代码，JS引擎会计算结果

- 2语法：{{表达式}}

  ![image-20230903160506825](C:\Users\18454\AppData\Roaming\Typora\typora-user-images\image-20230903160506825.png)

- 3.注意点

  (1)使用的数据必须存在(data要声明)

  ![image-20230903160524691](C:\Users\18454\AppData\Roaming\Typora\typora-user-images\image-20230903160524691.png)

  (2)支持表达式，而非语句。eg: if for ...

  ![image-20230903160536858](C:\Users\18454\AppData\Roaming\Typora\typora-user-images\image-20230903160536858.png)

  (3)不能在标签属性中使用{{}}插值

![image-20230903160545692](C:\Users\18454\AppData\Roaming\Typora\typora-user-images\image-20230903160545692.png)

# Vue核心特性：响应式

响应式：数据变化，视图自动更新。

![image-20230903165525236](C:\Users\18454\AppData\Roaming\Typora\typora-user-images\image-20230903165525236.png)

获取 实例名.属性

修改 实例名.属性=“内容”

# Vue指令

Vue会根据不同的**指令**，针对标签实现不同的**功能**。

指令：带有v-前缀的特殊标签属性

```
<div v-html="str"></div>
```

v-html:

作用：设置元素的innerHTML

语法：v-html="表达式"