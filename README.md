# Vue 3 + Vite
[Vue3](https://v3.cn.vuejs.org/guide/introduction.html)
[Vite](https://cn.vitejs.dev/)

## 使用Vite构建项目
npm:
```
# npm 6.x
$ npm init vite@latest <project-name> --template vue

# npm 7+，需要加上额外的双短横线
$ npm init vite@latest <project-name> -- --template vue

$ cd <project-name>
$ npm install
$ npm run dev
```
yarn:
```
$ yarn create vite <project-name> --template vue
$ cd <project-name>
$ yarn
$ yarn dev
```

# tips

### computed 和 methods 的区别
- computed 和 methods 的却别在于，computed会基于它的响应依赖关系进行缓存，只有当它依赖的值发生改变的时候重新计算，这也就意味着，只要它所以来的值没有发生变化，再次请求时，都会返回之前的值，而不必再次执行函数，而methods，每次触发重新渲染时，都会执行函数

### v-show 和 v-if 的区别
- v-show 只是简单地切换元素的 display
- v-if 是“真正”的条件渲染，因为它会确保在切换过程中，条件块内的事件监听器和子组件适当地被销毁和重建。
- v-if 也是惰性的：如果在初始渲染时条件为假，则什么也不做——直到条件第一次变为真时，才会开始渲染条件块。
- v-if 有更高的切换开销，而 v-show 有更高的初始渲染开销。因此，如果需要非常频繁地切换，则使用 v-show 较好；如果在运行时条件很少改变，则使用 v-if 较好。
