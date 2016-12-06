##computed与methods的比较
它们可以做同样的事情，比如计算复杂的逻辑返回结果。
从形式上的不同，computed在标签中使用它的名字就可以了，methods需要使用名字并加（）
性能上的不同，computed是基于缓存依赖，只有依赖关系发生变化才会去取值，消耗更少
methods当重新渲染的时候，总会调用函数，相比而言更准确，但是消耗大

##v-if与v-show的比较
v-if切换消耗大，v-show初次加载消耗大
如果不怎么切换的情况下，就用v-show
如果初次加载避免消耗的话，就用v-if

##v-html与v-text的比较
v-text会把data中的变量值全部按照字符串显示出来，包括标签如&lt;h1&gt;a&lt;/h1&gt;
v-html会将data中有标签的渲染成html，其他的字符串显示，上述标签就会是一级标题样式的a

##此时相当于对组件进行了重命名，可以有效可用的(comp和cpp都可用用)
var cp=Vue.component('comp',{
        template:'&lt;div&gt;哈哈1&lt;/div&gt;'
})
components:{
            'comp1':Child1,
            'cpp':cp
}

##特别注意##
HTML 特性不区分大小写。当使用非字符串模版时，prop的名字形式会从 camelCase 转为 kebab-case（短横线隔开）,
否则就会出现无效的情况

##界面抖动的问题
由于{{data}}会出现抖动的情况，可以用v-text="data" 或v-html="data"解决

###this.$emit('add');
相当于在父组件上定义了一个类似click的事件，还可以在add后加，参数。用于子组件向父组件传递数据

###注意：
new Vue({...})必须放在Vue.component('XXX', {...})之后，否则组件中的各种设置无效


##安装步骤
1.npm install -g vue-cli
2.vue init webpack my-project
3.cd my-project
4.npm install
5.npm run dev