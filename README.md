# <p align="center">vue2-vant2-components</p>

## 介绍
本库基于基值 375PX 开发，并依赖了部分 [vant](https://vant-contrib.gitee.io/vant/v2/#/zh-CN) 的功能。
[组件列表直通车](#components) | [指令列表直通车](#directives) | [浏览器适配直通车](#adapter)

## 浏览器支持
vue2-vant2-components 支持现代浏览器和 Android>=4.0、iOS>=8.0。

## 安装
使用 “npm” 安装：
```
npm i vue2-vant2-components -S
```

使用 “yarn” 或 “pnpm” ：
```bash
# with yarn
yarn add vue2-vant2-components

# with pnpm
pnpm add vue2-vant2-components
```

## 引入组件
### 方式一. 自动按需引入组件 (推荐)
[babel-plugin-import](https://github.com/umijs/babel-plugin-import) 是一款 babel 插件，它会在编译过程中将 import 的写法自动转换为按需引入的方式。
```js
# 安装插件
npm i babel-plugin-import -D
```
```js
# 安装插件
// 在.babelrc 中添加配置
// 注意：webpack 1 无需设置 libraryDirectory
{
  "plugins": [
    ["import", {
      "libraryName": "vue2-vant2-components",
      "libraryDirectory": "lib",
      "style": true
    }]
  ]
}

// 对于使用 babel7 的用户，可以在 babel.config.js 中配置
module.exports = {
  plugins: [
    ['import', {
      libraryName: 'vue2-vant2-components',
      libraryDirectory: 'lib',
      style: true
    }, 'vue2-vant2-components']
  ]
};
```

```js
// 接着你可以在代码中直接引入 vue2-vant2-components 组件
// 插件会自动将代码转化为方式二中的按需引入形式
import { vvcTable } from 'vue2-vant2-components';
```

```js
// 然后在main.js中引入公共样式
import 'vue2-vant2-components/lib/common';
```

### 方式二. 手动按需引入组件
在不使用插件的情况下，可以手动引入需要的组件。
```js
import Button from 'vue2-vant2-components/lib/vvc-table';
import 'vue2-vant2-components/lib/vvc-table/style';
```

```js
// 然后在main.js中引入公共样式
import 'vue2-vant2-components/lib/common';
```

### 方式三. 导入所有组件
```js
import Vue from 'vue';
import vvc from 'vue2-vant2-components';
import 'vue2-vant2-components/lib/index/style.css';

Vue.use(vvc);
```

查看更多有关信息 [链接](https://github.com/317883224/vue2-vant2-components).

## 组件列表<a id="components"></a>
|    组件    |                                     说明                                      |                    文档                     |
| :--------: | :---------------------------------------------------------------------------: | :-----------------------------------------: |
|   Select   |                                    选择器                                     |     [文档](./markdown/select/select.md)     |
|   Table    | 表格组件，与 TabulationCell 不同， 该组件为一列一列的数据，为 table 标签封装  |      [文档](./markdown/table/table.md)      |
| Tabulation | 表格组件，与 Table 排版不同，该组件为 key: value 和 flex 组合为一行一行的数据 | [文档](./markdown/tabulation/tabulation.md) |
| datePicker |                                日期选择器组件                                 | [文档](./markdown/datePicker/datePicker.md) |
|   upload   |                                 上传文件组件                                  |     [文档](./markdown/upload/upload.md)     |
|  zoomList  |                                 缩放列表组件                                  |     [文档](./markdown/zoomList/zoomList.md)     |

## 指令列表<a id="directives"></a>
|   指令    |     说明     |                   文档                    |
| :-------: | :----------: | :---------------------------------------: |
|  loading  | 加载状态指令 |   [文档](./markdown/loading/loading.md)   |
| longpress |   长按指令   | [文档](./markdown/longpress/longpress.md) |

## 浏览器适配<a id="adapter"></a>

### Viewport 布局

vue2-vant2-components 默认使用 `px` 作为样式单位，如果需要使用 `viewport` 单位 (vw, vh, vmin, vmax)，推荐使用 [postcss-px-to-viewport](https://github.com/evrone/postcss-px-to-viewport) 进行转换。

[postcss-px-to-viewport](https://github.com/evrone/postcss-px-to-viewport) 是一款 PostCSS 插件，用于将 px 单位转化为 vw/vh 单位。

#### PostCSS PostCSS 示例配置

下面提供了一份基本的 PostCSS 示例配置，可以在此配置的基础上根据项目需求进行修改。

```js
// postcss.config.js
module.exports = {
  plugins: {
    'postcss-px-to-viewport': {
      viewportWidth: 375,
    },
  },
};
```

> Tips: 在配置 postcss-loader 时，应避免 ignore node_modules 目录，否则将导致 vue2-vant2-components 样式无法被编译。

### Rem 布局适配

如果需要使用 `rem` 单位进行适配，推荐使用以下两个工具：

- [postcss-pxtorem](https://github.com/cuth/postcss-pxtorem) 是一款 PostCSS 插件，用于将 px 单位转化为 rem 单位
- [lib-flexible](https://github.com/amfe/lib-flexible) 用于设置 rem 基准值

#### PostCSS 示例配置

下面提供了一份基本的 PostCSS 示例配置，可以在此配置的基础上根据项目需求进行修改。

```js
// postcss.config.js
module.exports = {
  plugins: {
    'postcss-pxtorem': {
      rootValue: 37.5,
      propList: ['*'],
    },
  },
};
```

> Tips: 在配置 postcss-pxtorem 时，同样应避免 ignore node_modules 目录，否则会导致 vue2-vant2-components 样式无法被编译。

#### 其他设计稿尺寸

如果设计稿的尺寸不是 375，而是 750 或其他大小，可以将 `rootValue` 配置调整为:

```js
// postcss.config.js
module.exports = {
  plugins: {
    // postcss-pxtorem 插件的版本需要 >= 5.0.0
    'postcss-pxtorem': {
      rootValue({ file }) {
        return file.indexOf('vue2-vant2-components') !== -1 ? 37.5 : 75;
      },
      propList: ['*'],
    },
  },
};
```

## 补充
当出现解析错误时使用：
```js
module.exports = {
  transpileDependencies: ['vue2-vant2-components'],
}
```

## LICENSE
vue2-vant2-components is [MIT](https://en.wikipedia.org/wiki/MIT_License) licensed.

## 引用
[vant](https://vant-contrib.gitee.io/vant/v2/#/zh-CN)