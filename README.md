# [lijoyui](http://192.168.1.109:4873/)



> It's a A personal Vue UI component library .

## 准备工作
安装npm私有仓库框架verdaccio
```js
npm install --global verdaccio@6-next --registry https://registry.verdaccio.org/
```
安装完成后直接运行命令
```js
verdaccio
```
输入http://localhost:4873，就可以看到页面
![image](https://github.com/Lingtian007/Vue-demo/assets/48399168/78d77005-c830-4608-aa16-0c982913c92b)

+注意:

>Verdaccio默认是localhost，要使用ip给其它电脑访问，可在config.yaml 文件中添加一行 listen: 0.0.0.0:4873 ，在Verdaccio启动的第一行有config.yaml的地址，编辑文件在最后一行加入listen: 0.0.0.0:4873

>其他教程说是启动时可以查看界面的warn警告可以看到config配置文件的地址
但作者启动时没有找到warn ，所以直接用everything搜索 config.yaml
作者的配置文件的地址为
C:\Users\Administrator\AppData\Roaming\verdaccio\config.yaml。

然后重启服务就可以生效
如果嫌麻烦可以直接重启电脑

这样可以在其他电脑上设置仓库地址 npm set registry http://ip:4873/

## 安装

### npm 安装

```shell
npm i  lijoyui  --registry http://192.168.1.109:4873/
```
### 发布版本

```shell
 nrm 切换到 别名:http://192.168.1.109:4873/
 + 发布前请修改版本号
 npm publish
```
### 删除版本(请在24小时内删除)

```shell
npm unpublish lijoyui@版本号 --registry http://192.168.1.109:4873/ --force
```

## 快速开始

### 完整引入

```javascript
import Vue from 'vue'
import Vui from "lijoyui";
import "lijoyui/lib/vui-css/index.css";


Vue.use(Vui)
```

### 部分引入

```javascript
import Vue from 'vue'
import {
  Scroller,
  Select
  // ...
} from 'lijoyui'
import 'lijoyui/lib/vui-css/scroller.css';
import 'lijoyui/lib/vui-css/select.css';

Vue.component(Scroller.name, Scroller)
Vue.component(Select.name, Select)
```

### 引入插件

**注：完整引入了vui，则无需再注册插件**

```javascript
import Vue from 'vue';
import { 
  $Toast, 
  $Dialog 
  // ...
} from 'lijoyui';

Vue.prototype.$toast = $Toast
Vue.prototype.$dialog = $Dialog
```
 



