# Vue 在线翻译(translate)
> 由 Vue 搭建的 在线翻译工具
---

# 项目详情
> - 由 Vue2.0 搭建，接入Translate API，包含47中语言，满足日常翻译需要


---

# 项目构建思路
> ###   项目环境： Node.js (v.8.4.0)  npm (5.3.0)  vue (2.9.1)  vue-cli ()
``` bash
1. 建立一个文件夹，取名为你的项目名称
2. 执行命令安装vue-cli ,  npm install --global vue-cli
3. 打开Git Bash ， 输入 vue init webpack , 建立vue的基本文件。
4. 执行npm install ， 下载依赖包。
5. 执行npm run dev ， 运行项目。
```

---
# 项目构建思路
``` bash
1. 建立 '输入'' 组件，建立 '输出结果'' 组件
2. 将组件插入 app.vue 根组件中
3. 编写输入输出组件基本内容
4. 引入 Translate API ， 编写格式，将需要翻译的文本提交到 Translate 中
5. 从 Translate 返回的翻译内容。 插入到 '输出结果' 组件。
6. 最后把引入 Bootstrap.css 美化基本样式。
7. 项目打包，提交GitHub
```

---
# 项目下载安装
``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

```


