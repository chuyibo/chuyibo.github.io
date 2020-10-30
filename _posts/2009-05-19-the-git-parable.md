---
layout: post
title: 前端自动化构建工具 - Webpack 使用（一）- 构建 CSS 模块
---

{{ page.title }}
================

<p class="meta">19 May 2009 - San Francisco</p>
1.创建样式模块

<pre><div id="code">div {
    background: blue;
}
</div></pre>

2.创建 JavaScript 模块

<pre><div id="code">import './index.css'
...
</div></pre>

3.创建配置文件

<pre><div id="code">var path = require('path');

module.exports = {
    entry: './index.js',
    output: {
        path: path.resolve(__dirname, ''),
        filename: 'bundle.js'
    },
    module: {
        rules: [{
            test: /\.css$/,
            use: ['style-loader', 'css-loader']
        }]
    },
    mode: 'none'
};
</div></pre>

