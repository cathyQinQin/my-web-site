<template>
  <h2 class="article-introduction">Here’s a few study notes I’ve wrote on Blog:</h2>
  <div class="articles-main">
    <section v-for="article in articles" 
            :key="article.id" 
            aria-label="Glasgow Disability Alliance" 
            class="article article--linked ">
      <header class="article-header">
        <h3 class="article-title">Glasgow Disability Alliance</h3>
        <div class="article-detail">werewrwerwerwerwerwerwerwerwerwrwerwrwrwrwrwrwrwrwrwrwrwrwer</div>
      </header>
      <div class="article-footer">March 2021</div>
      
      <a href="https://gda.scot/" target="_blank" rel="noopener" class="article__link"> </a>
    </section>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'article',
  setup() {
    const articles = ref([1,2]);
    return {
      articles,
    } // 这里返回的任何内容都可以用于组件的其余部分
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');
  .article-introduction
    font-family: 'Roboto', sans-serif;
    color #444
    padding 1rem 10% 
    text-align center
  .articles-main
    color #444
    display flex
    flex-flow column
    margin 0 10%
    justify-content space-between
    section
      margin-bottom 2rem
      box-sizing border-box
      position relative
      background-color #fff
      border-radius: 8px
      display flex
      flex-direction column
      .article__link 
        position absolute
        top: 0
        left: 0
        right: 0
        bottom: 0
        border-radius: 8px
        transition border .16667s ease
        box-shadow 1px 3px 5px 4px rgba(204,204,204,0.75)
      .article__link:hover
        border 2px solid #aaa
      .article-header
        flex 0 0 75%
        display flex
        flex-direction column
        padding 0.5rem 2rem
      .article-footer
        flex 0 0 25%
        border-top 1px solid #eee
        padding-top .875rem
        padding-bottom .875rem
        font-size .875rem
        padding 0.5rem 2rem
       
    
        
</style>
