<template>
  <header>
    <section class="autowidth tagline">Hey There, I'm Qin Zhang,</section>
    <section class="autowidth desc">based in Edmonton, Canada.</section>
    <section class="autowidth tagline">Just Another Master's student.</section>
    <section class="autowidth desc">Studying at University of Alberta.</section>
    <section class="autowidth tagline">And know a lot about coding.</section>
    <section class="autowidth desc last-header">But just want a chance to work as intern. 😝</section>
  </header>
</template>

<script>
export default {
  name: 'Introduction',
  setup() {
    return {
      
    } // 这里返回的任何内容都可以用于组件的其余部分
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  header
    margin-top 5rem
    .autowidth
      margin 0 15%
      height 3rem
    .tagline
      color #444
      font-size 3rem
      text-align left
      font-weight 700
    .desc
      text-align left
      font-size 1.25rem
      color: #ccc
      font-weight 300
      line-height 1.3
      padding 1rem 0 1rem
</style>
