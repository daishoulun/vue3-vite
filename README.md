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
- computed 和 methods 的却别在于，computed会基于它的响应依赖关系进行缓存，只有当它依赖的值发生改变的时候重新计算，这也就意味着，只要它所以来的值没有发生变化，再次请求时，都会返回之前的值，而不必再次执行函数，而methods，每次触发重新渲染时，都会执行函数
