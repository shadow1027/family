## 使用 umi 搭建项目记录

### 初始化项目
* 创建一个文件夹 
```bash
mkdir myapp
```
* 进入该文件夹，并初始化
```bash
cd myapp
npm init -y
```
* 安装相关依赖
```bash
cnpm install umi --save-dev
cnpm install dva --save
cnpm install umi-plugin-react --save-dev
```
* 配置启动命令 `package.json`
```js
...
"scripts": {
  "dev": "umi dev",
  "build": "umi build"
}
...
```
* 配置git忽略文件`.gitignore`
```
node_modules
dist
.umi
```
* 配置`.umirc.js`
```js
export default {
  plugins: [
    ['umi-plugin-react', {
      antd: true, // 使用 antd
    }]
  ]
}
```

### 配置页面布局
在`src`目录下添加`layouts`文件夹，然后创建`index.js`，这个文件里面放置的是表示全局布局。
`umi`中集成了`less`，不需要额外配置就可以使用。