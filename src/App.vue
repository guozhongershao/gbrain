<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  import '../static/font/iconfont.css'
  export default {
    name: 'App'
  }
</script>

<style>
  /* 清除内外边距 */
  body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, /* structural elements 结构元素 */
  dl, dt, dd, ul, ol, li, /* list elements 列表元素 */
  pre, /* text formatting elements 文本格式元素 */
  fieldset, lengend, button, input, textarea, /* form elements 表单元素 */
  th, td { /* table elements 表格元素 */
    margin: 0;
    padding: 0;
  }

  /* 设置默认字体 */
  body,
  button, input, select, textarea { /* for ie */
    /*font: 12px/1 Tahoma, Helvetica, Arial, "宋体", sans-serif;*/
    font: 12px/1 Tahoma, Helvetica, Arial, "\5b8b\4f53", sans-serif; /* 用 ascii 字符表示，使得在任何编码下都无问题 */
  }

  h1 {
    font-size: 18px; /* 18px / 12px = 1.5 */
  }

  h2 {
    font-size: 16px;
  }

  h3 {
    font-size: 14px;
  }

  h4, h5, h6 {
    font-size: 100%;
  }

  address, cite, dfn, em, var {
    font-style: normal;
  }

  /* 将斜体扶正 */
  code, kbd, pre, samp, tt {
    font-family: "Courier New", Courier, monospace;
  }

  /* 统一等宽字体 */
  small {
    font-size: 12px;
  }

  /* 小于 12px 的中文很难阅读，让 small 正常化 */

  /* 重置列表元素 */
  ul, ol {
    list-style: none;
  }

  /* 重置文本格式元素 */
  a {
    text-decoration: none;
    color: inherit;
  }

  abbr[title], acronym[title] { /* 注：1.ie6 不支持 abbr; 2.这里用了属性选择符，ie6 下无效果 */
    border-bottom: 1px dotted;
    cursor: help;
  }

  q:before, q:after {
    content: '';
  }

  /* 重置表单元素 */
  legend {
    color: #000;
  }

  /* for ie6 */
  fieldset, img {
    border: none;
  }

  /* img 搭车：让链接里的 img 无边框 */
  /* 注：optgroup 无法扶正 */
  button, input, select, textarea {
    font-size: 100%; /* 使得表单元素在 ie 下能继承字体大小 */
  }

  /* 重置表格元素 */
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }

  /* 重置 hr */
  hr {
    border: none;
    height: 1px;
  }

  body {
    background-color: white;
  }

  /* 自定义滚动条样式 */
  /*定义滚动条高宽及背景 高宽分别对应横竖滚动条的尺寸*/
  ::-webkit-scrollbar {
    width: 6px; /*滚动条宽度*/
    height: 5px; /*滚动条高度*/
  }

  /*定义滚动条轨道 内阴影+圆角*/
  ::-webkit-scrollbar-track {
    /*-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);*/
    /*border-radius: 10px;  !*滚动条的背景区域的圆角*!*/
    background-color: #e5e5e5; /*滚动条的背景颜色*/
  }

  /*定义滑块 内阴影+圆角*/
  ::-webkit-scrollbar-thumb {
    /*border-radius: 3px;  !*滚动条的圆角*!*/
    /*-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);*/
    background-color: #797979; /*滚动条的背景颜色*/
  }
</style>
