# kbone
一个基于 Kbone for React、TypeScript、Less 的跨端模板库。

## 快速开始
```shell script
# clone 模板
git clone https://github.com/LeiHanCN/kbone.git <your-project-path>

# 进入到进本目录下执行初始化脚本
cd <your-project-path>/srcipts
chmod 777 init.sh
./init.sh
cd ..

# 安装依赖
yarn 
# 开发小程序
yarn dev:miniapp 
# 打包
yarn build:miniapp
# 开发 Web
yarn dev:web
# 打包 Web
yarn build:web
```

## 特性
使用 react 多端开发(小程序和 Web)，基于 [kbone](https://github.com/wechat-miniprogram/kbone) 的 element 和 render。

webpack、hook、es2018+、babel7+、jsx、hot reload、cli...


## 目录说明

```
├─ build
│  ├─ mp     //微信开发者工具指向的目录，用于生产环境
│  ├─ web    //web 编译出的文件，用于生产环境
├─ config
├─ public
├─ scripts
├─ src
│  ├─ assets
│  ├─ components    //存放所有组件
│  ├─ log.js        //入口文件，会 build 成  log.html
│  └─ index.js      //入口文件，会 build 成  index.html
```

## 注意事项

react 并没有提供根组件实例的销毁方法（如 vue.$destroy），所以在多页应用中页面关闭时不会触发该页面组件的 componentWillUnmount 钩子。开发者可自行监听 wxunload 或 beforeunload 事件来进行页面的销毁工作，比如调用 render 方法渲染一个空节点，强行触发页面组件的 componentWillUnmount 钩子。

## License

MIT 
