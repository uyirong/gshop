<template>
  <header class="header">
    <slot name="search"></slot>
    <a class="header_title"> <span class="header_title_text ellipsis">{{title}}</span> </a>
    <slot name="login"></slot>
  </header>
</template>
<script> export default {props: {title: String}} </script>
<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixins.styl"
  .header {
    background-color: #02a774;
    position: fixed;
    z-index: 100;
    left: 0;
    top: 0;
    width: 100%;
    height: 45px;
  }
  .header .header_search {
    position: absolute;
    left: 15px;
    top: 50%;
    transform: translateY(-50%);
    width: 10%;
    height: 50%;
  }
  .header .header_search .iconfont {
    font-size: 22px;
    color: #fff;
  }
  .header .header_title {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 30%;
    color: #fff;
    font-size: 22px;
    text-align: center;
  }
  </style>
