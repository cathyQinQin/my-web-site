<template>
  <div class="article-section">
    <h2 class="article-introduction">Here’s a few study notes I’ve wrote on Blog:</h2>
    <div class="articles-main">
      <section v-for="(item, index) in articles" 
              :key="index" 
              aria-label="Glasgow Disability Alliance" 
              class="article article--linked ">
        <header class="article-header">
          <h3 class="article-title">{{item.title}}</h3>
          <div class="article-detail">{{item.content}}</div>
        </header>
        <div class="article-footer">{{item.time}}</div>
        
        <a :href="item.url" target="_blank" rel="noopener" class="article__link"> </a>
      </section>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import axios from 'axios'
export default {
  name: 'Article',
  setup() {
    const articles = ref([])
    const getInfo = async() => {
      articles.value = await axios
      .get('info.json')
      .then(response => response.data)}
    getInfo()
    return {
      articles,
    } // 这里返回的任何内容都可以用于组件的其余部分
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  .article-section
    margin 2rem 10%
    .article-introduction
      font-family: 'Roboto', sans-serif;
      color #444
      text-align center
      padding-bottom 2rem
    .articles-main
      color #444
      display flex
      flex-flow column
      justify-content space-between
      border-bottom 1px solid #ddd
      section
        font-family: 'Montserrat', sans-serif;
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
          box-shadow 0px 8px 16px rgba(204,204,204,0.75)
        .article__link:hover
          border 2px solid #aaa
        .article-header
          flex 0 0 75%
          display flex
          flex-direction column
          padding 2rem 2rem
          .article-title
            padding-bottom 1rem
            font-family: 'Roboto', sans-serif;
          .article-detail
            overflow hidden
            text-overflow ellipsis
            display -webkit-box
            -webkit-box-orient vertical
            -webkit-line-clamp 2   
        .article-footer
          flex 0 0 25%
          border-top 1px solid #eee
          font-size .875rem
          padding 0.75rem 2rem
</style>
