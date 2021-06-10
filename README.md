<!--
 * @Author: zhangyu
 * @Email: zhangdulin@outlook.com
 * @Date: 2021-06-08 11:30:40
 * @LastEditors: zhangyu
 * @LastEditTime: 2021-06-10 18:24:09
 * @Description:
-->

[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)
[![Eclipse Marketplace](https://img.shields.io/eclipse-marketplace/dt/notepad4e.svg)](https://www.npmjs.com/package/jslib-tools)
![NpmVersion](https://img.shields.io/npm/v/npm.svg)

### Description:

前端 js 工具库: 封装常用的工具函数，如日期格式化、浏览器判断等，提高开发效率

## Todo

- [√] 引入代码校验工具 eslint
- [√] jsdocs typedocs 自动化生成 api 文档
- [√] 测试覆盖率统计 coverage
- [√] 支持Typescript
- [√] 支持浏览器环境，node 环境、es6 环境

### 如何使用:

1. 直接下载 `dist` 目录下的 `jtools.min.js` 使用，支持 UMD 通用模块规范
2. 使用 npm 安装

#### 浏览器：

```js
<script src="jtools.min.js"></script>
<script>
    var result = jtools.add(1, 2)
</script>
```

#### npm:

`npm i jslib-tools`

##### 全部加载（webpack、RequireJS、SeaJS 等）：

```js
var jtools = require("jslib-tools");
var result = jtools.add(1, 2);
```

#### es6

```js
import jtools from "jslib-tools";
var result = jtools.add(1, 2);
```

### 按需加载

结合[babel-plugin-import-load](https://github.com/Pasoul/babel-plugin-import-load)按需加载可以极大的减小依赖包的体积

```js
import { add } from "jslib-tools";
var result = add(1, 2);
```

#### 自动化生成文档

[JSDoc](http://www.css88.com/doc/jsdoc/about-configuring-jsdoc.html)是一个根据 javascript 文件中注释信息，生成 JavaScript 应用程序或库、模块的 API 文档 的工具。你可以使用他记录如：命名空间，类，方法，方法参数等。类似 JavaDoc 和 PHPDoc。现在很多编辑器或 IDE 中还可以通过 JSDoc 直接或使用插件生成智能提示。从而使开发者很容易了解整个类和其中的属性和方法，并且快速知道如何使用，从而提高开发效率，降低维护成本。

`yarn run doc`

### 扩展

如果你想添加自己的工具库，在 `src` 目录创建文件，对应 `test` 目录添加测试用例，执行 `yarn test`
