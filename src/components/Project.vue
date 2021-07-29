<template>
  <h2 class="project-introduction">Here’s a few projects I’ve worked on:</h2>
  <div class="projects-main">
    <section v-for="project in projects" 
            :key="project.id" 
            aria-label="Glasgow Disability Alliance" 
            class="project project--linked ">
      <header class="project-header">
        <h3 class="project-title">Glasgow Disability Alliance</h3>
      </header>
      <dl class="project-detail project__details">
        <dt class="project-detail__title"> Designer</dt>
        <dd class="project-detail__item"> Lewis Dorigo</dd>
        <dt class="project-detail__title"> Launch Date</dt>
        <dd class="project-detail__item"> 
          <time datetime="2021-03-22">March 2021</time>
        </dd>
      </dl>
      <a href="https://gda.scot/" target="_blank" rel="noopener" class="project__link"> </a>
    </section>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Project',
  setup() {
    const projects = ref([1,2,3,4]);
    return {
      projects,
    } // 这里返回的任何内容都可以用于组件的其余部分
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');
  .project-introduction
    font-family: 'Roboto', sans-serif;
    color #444
    padding 1rem 10% 
    text-align center
  .projects-main
    color #444
    display flex
    flex-flow row wrap
    margin 0 10%
    justify-content space-between
    border-bottom 1px solid #ddd
    section
      height 60vh
      margin-bottom 5%
      box-sizing border-box
      flex 0 0 30%
      position relative
      background-color #fff
      border-radius: 8px
      display flex
      flex-direction column
      .project__link 
        position absolute
        top: 0
        left: 0
        right: 0
        bottom: 0
        border-radius: 8px
        transition border .16667s ease
        box-shadow: 1px 3px 5px 4px rgba(204,204,204,0.75);
      .project__link:hover
        border 2px solid #aaa
        
      .project-header
        flex 0 0 45%
        display flex
        justify-content center
        align-items center
        border-bottom 1px solid #eee
      .project-detail
        flex 0 0 55%
        padding: 1.75rem 2rem;
        .project-detail__title
          font-weight 700
          text-transform uppercase
          letter-spacing .333rem
        .project-detail__item
          font-weight 200
          margin-inline-start 0
          margin-bottom 1rem
        
</style>
