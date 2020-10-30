---
layout: post
title: 前端自动化构建工具 - webpack 使用（一）
---

前端自动化构建工具 - webpack 使用（一）- 构建 css 样式
================

<p class="meta">30 Oct 2020 - zhengzhou</p>

<pre><div id="code">npm install webpack webpack-cli -D
npm install css-loader style-loader -D
</div></pre>

<pre><div id="code">div {
    background: blue;
}
</div></pre>

<pre><div id="code">import './index.css'
...
</div></pre>

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

<p alient="justify">css-loader 能够解析 css 文件，以字符串的形式打包进 js 文件中，css-loader 的打包结果作为 style-loader 的参数，stype-loader 通过动态生成 stype 标签的形式将字符串样式代码插入到 HTML 文件中。</p>

