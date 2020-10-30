---
layout: post
title: 前端自动化构建工具 - Webpack 使用（一）- 构建 CSS 模块
---

{{ page.title }}
================

<p class="meta">30 Oct 2020 - zhengzhou</p>

<pre><div id="code">div {
    background: blue;
}
</div></pre>

<div heigth: 40px></div>

<pre><div id="code">import './index.css'
...
</div></pre>

<div heigth: 40px></div>

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

