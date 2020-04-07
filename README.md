# [lijoyui](http://192.168.1.109:4873/)



> It's a A personal Vue UI component library .

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
 
## 贡献代码


