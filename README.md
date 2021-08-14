# vue-examples
Learn official vue examples

# 试试SSH连接是否成功  2021/08/11



# add vue-20-github-commits  2021/08/12

1. #### [表单输入绑定](https://cn.vuejs.org/v2/guide/forms.html)  input 用  `v-model="checked"`绑定

2. #### [侦听器](https://cn.vuejs.org/v2/guide/computed.html) watch函数用法

   ```js
   watch: {   currentBranch: "fecthData"   }  //监听到 currentBranch 改变就运行 fecthData 函数
   ```

3. #### filters 过滤器

   [过滤器](https://cn.vuejs.org/v2/guide/filters.html) 用于一些常见的文本格式化

   ```html
   <!-- 在双花括号中 -->
   <!-- {{ 要格式化的数据 | 对数据格式化的方法 }} -->
   {{ message | capitalize }}    
   
   <!-- 在 `v-bind` 中 -->
   <div v-bind:id="rawId | formatId"></div>
   ```

   ```js
   本地过滤器：filters: {  }
   
   全局过滤器：Vue.filter('capitalize', function (value) {})
   ```



# add grid 2021/08/13

#### Vue组件 props

props down, events up。父组件通过 props 向下传递数据给子组件，子组件通过 events 给父组件发送消息。

### x-template

将html结构写在一对script标签中，设置type=“x-template”

[Vue X-Template](https://cn.vuejs.org/v2/guide/components-edge-cases.html#X-Template)

> 这些可以用于模板特别大的 demo 或极小型的应用，但是其它情况下请避免使用，因为这会将模板和该组件的其它定义分离开。



#  add tree view 2021/08/14

[组件的递归使用 ](https://cn.vuejs.org/v2/guide/components-edge-cases.html#%E9%80%92%E5%BD%92%E7%BB%84%E4%BB%B6) ：确保递归调用是条件性的 (例如使用一个最终会得到 `false` 的 `v-if`)

遇错：

```shell
Component template requires a root element, rather than just text
```

其实就是注册组件的时候没挂载好id，错误：`template: "cpn1"` , 正确：`template: "#cpn1"`

