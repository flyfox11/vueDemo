##computed与methods的比较
它们可以做同样的事情，比如计算复杂的逻辑返回结果。
从形式上的不同，computed在标签中使用它的名字就可以了，methods需要使用名字并加（）
性能上的不同，computed是基于缓存依赖，只有依赖关系发生变化才会去取值，消耗更少
methods当重新渲染的时候，总会调用函数，相比而言更准确，但是消耗大

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


##安装步骤
1.npm install -g vue-cli
2.vue init webpack my-project
3.cd my-project
4.npm install
5.npm run dev