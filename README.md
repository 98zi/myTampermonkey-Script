## myTampermonkey-Script

自用的油猴脚本，可能不适用于其他场景，可自行修改。

基于 vue 的油猴脚本模板: [https://github.com/98zi/tampermonkey-template](https://github.com/98zi/tampermonkey-template)

- [v2ex 图片灯箱插件](./v2ex图片灯箱插件.js)
- [feedly 汉化脚本](./feedly汉化脚本.js)
- [Netlify 汉化脚本](./Netlify汉化脚本.js)
- [douyin 下载](./douyin下载.js)

## 初始化模板

```js
// ==UserScript==
// @name         Tampermonkey Nmae
// @namespace    https://github.com/98zi/myTampermonkey-Script
// @version      0.0.1
// @description  Tampermonkey description
// @author       98zi
// @match        http://*/*
// @match        https://*/*
// @icon         https://www.google.com/chrome/static/images/chrome-logo-m100.svg
// @require      https://cdn.bootcss.com/jquery/3.6.0/jquery.min.js
// @grant        none
// @license      MIT
// ==/UserScript==

(function () {
  'use strict';
  // 替换
  if (location.href === "http://localhost:8080/") return
  let script = document.createElement('script')
  script.src = 'http://localhost:8080/app.bundle.js'
  document.body.appendChild(script)
  // 替换
})();
```

本地运行后显示 `Compiled successfully.` 即为成功，打开 `http://localhost:8080/` 可以看到一个示例 demo。

```shell
npm install

npm start
```

## 开发脚本


