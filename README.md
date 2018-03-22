# Vue/life cycle hook

Vue. Js life cycle.

Each Vue instance goes through a series of initialization processes before being created. For example, you need to set the data listener, compile the template, mount the instance to the DOM, update the DOM when the data changes. It also runs some functions called life cycle hooks, giving users the opportunity to add their own code to certain scenarios.

Vue 2.0 official life cycle hook function.

BeforeCreate -- the component instance has just been created.

Created - the component instance creation is complete.

BeforeMount -- before the template is compiled or mounted.

Mounted - after the template is compiled or mounted.

BeforeUpdate -- before the component instance is updated.

Updated - after the component instance is updated.

Activated -- the component instance is invoked when it is activated.

Deactivated - when a component instance is removed.

BeforeDestroy -- before the component instance is destroyed.

Destroyed - after the component instance is destroyed.

Create a Vue instance

New Vue ({... })

The four hook functions you need to master.

Created ()

After the instance creation is completed, it is called immediately. However, the mount phase has not yet started and the el attribute is currently not visible.

Mounted ()

The el is replaced by the newly created vm. El, and the hook is called after it is mounted to the instance.

BeforeUpdate () and updated ()

The two are a pair. When you change the data, that is, when you change the data in the vue instance, the two are triggered separately.

** the difference between created ** and ** mounted **.

Create () gets the data earlier.

Mounted () can manipulate documents, created() not.

Beforecreated: el and data are not initialized.

Created: completes the initialization of data data, el does not.

BeforeMount: completes el and data initialization.

Mounted: complete the mount.

Component update: app.message = 'update content ';

Component destruction: app.$destroy();

---------------------------------------------

Vue.js 生命周期

每个 Vue 实例在被创建之前都要经过一系列的初始化过程。例如需要设置数据监听、编译模板、挂载实例到 DOM 、在数据变化时更新 DOM 等。同时在这个过程中也会运行一些叫做 生命周期钩子 的函数，给予用户机会在一些特定的场景下添加他们自己的代码。

Vue 2.0 官方生命周期钩子函数
beforeCreate -- 组件实例刚被创建
created -- 组件实例创建完成
beforeMount -- 模板编译或挂载之前
mounted -- 模板编译或挂载之后
beforeUpdate -- 组件实例更新之前
updated -- 组件实例更新之后
activated -- 组件实例被激活时调用
deactivated -- 组件实例被移除时调用
beforeDestroy -- 组件实例销毁前调用
destroyed -- 组件实例销毁后调用


创建 Vue 实例

new Vue ({...})


需要掌握的四个 钩子函数

created()

在实例创建完成后被立即调用. 然而，挂载阶段还没开始，el 属性目前不可见

mounted()

el 被新创建的 vm.el 替换，并挂载到实例上去之后调用该钩子

beforeUpdate() 和 updated()

两者是一对。当你改变数据的时候，也就是改变 vue 实例里面的 data 时，这两者会分别触发

** created ** 与 ** mounted ** 的区别

create() 获取数据要早一点
mounted() 可以操作文档，created() 不行

beforecreated：el 和 data 并未初始化
created:完成了 data 数据的初始化，el没有
beforeMount：完成了 el 和 data 初始化
mounted ：完成挂载

组件更新: app.message = '更新内容';

组件销毁: app.$destroy();
