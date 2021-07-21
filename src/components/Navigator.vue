<template>
  <nav>
    <div class="autowidth header-nav">
      <div class="logo">
        <img src="http://s.anw.red/iconmoon-2017/images/logo.png">
      </div>
      <ul>
        <li><a class="left-to-right" href="#works">Works</a></li>
        <li><a class="left-to-right" href="#about">About</a></li>
        <li class="nav-blog"><a class="left-to-right" href="http://IconMoon.com/blog2/" target="_blank">Blog</a></li>
        <li><a class="left-to-right" href="https://Anyway.FM/index.php?s=iconmoon" target="_blank">Podcast</a></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navigator',
  setup() {
    return {

    } // 这里返回的任何内容都可以用于组件的其余部分
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  .autowidth
    display flex
    justify-content space-between
    align-items center
    margin 0 15%
    height 3rem
    border 1px solid #fff
    border-bottom 1px solid #ddd
    transition all .4s cubic-bezier(.4,0,0,1)
    .logo img
      max-height 2rem
    ul
      display: flex;
      li
        padding 0 0.5rem
        font-size: 0.625rem;
        .left-to-right
          position relative
        .left-to-right::after
          display block
          content: "";
          width: 0;
          height: 1px;
          position: absolute;
          left: 0;
          top: 1.25rem;
          transition: all .2s cubic-bezier(1,0,0,1);
          border-bottom: .1em solid #777;
        .left-to-right:hover::after
          width 100%
</style>
