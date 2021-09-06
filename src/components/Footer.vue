<template>
  <footer
    aria-label="Site Footer"
    class="site-foot section section--flush-after wrap"
  >
    <a href="https://github.com/cathyQinQin" class="site-foot__link">
      <img src="http://s.anw.red/iconmoon-2017/images/logo.png" />
      <div>Designed and built by Qin.</div>
    </a>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  setup() {
    return {}; // 这里返回的任何内容都可以用于组件的其余部分
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
@import (css) url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

.site-foot {
  font-family: 'Montserrat', sans-serif;
  font-size: 0.85rem;
  margin: 0 38%;

  .site-foot__link {
    padding: 0.4rem 1.875rem;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #eee;
    border-radius: 8px 8px 0 0;
    text-decoration: none;
    transition: background-color 0.16667s ease, margin-top 0.16667s ease, padding-bottom 0.16667s ease;

    img {
      height: 2.5rem;
      margin-right: 1rem;
    }
  }

  .site-foot__link:hover {
    background: #e1e1e1;
    margin-top: -0.25rem;
    padding-bottom: 0.75rem;
  }
}
</style>
