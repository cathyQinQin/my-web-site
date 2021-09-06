<template>
  <article class="item about about-1" id="about">
    <div class="inner-item">
      <div class="item-main autowidth">
        <h1 class="item-text"><strong>About</strong> Me</h1>
        <div class="item-desc">
          <div>
            Although I work as a graduate teaching assistant and participate in
            open-source project <strong> Review Board </strong> and previously
            worked as a student researcher at U of A for 8 months, I am still
            looking for a chance to be an intern in a real company😅
          </div>
          <div>
            I live in Edmonton and currently study at
            <a href="https://www.ualberta.ca/index.html" target="_blank"
              >U of A</a
            >
            as a graduate student. When I'm not working, I love solving problems
            on
            <a href="https://leetcode-cn.com/u/zhang-qin-x/" target="_blank"
              >leetcode</a
            >
            and watching movies.
          </div>
        </div>
      </div>
      <div class="item-main autowidth contact-section">
        <h1 class="item-text"><strong>Contact</strong> Me</h1>
        <div class="item-desc">
          <a href="mailto:qin7@ualberta.ca">qin7@ualberta.ca</a> · E-mail<br /><br />
          <div class="social-list">
            <a
              target="_blank"
              href="https://www.linkedin.com/in/zhang-qin-ba02a8133/"
              >LinkedIn</a
            >
            /
            <a target="_blank" href="https://github.com/cathyQinQin">Github</a>
            /
            <a target="_blank" href="https://www.instagram.com/cathy_qin_qin/"
              >Instagram</a
            >
          </div>
        </div>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: "AboutMe",
  setup() {
    return {}; // 这里返回的任何内容都可以用于组件的其余部分
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
@import (css) url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap");
#about {
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
  margin: 0 15%;
  .inner-item {
    padding: 5rem 0;
    .contact-section {
      margin-top: 2rem;
    }
    .autowidth {
      font-family: "Roboto", sans-serif;
      display: flex;
      color: #333;
      .item-text {
        flex: 35%;
        font-size: 2.25rem;
        font-weight: 200;
        margin: 0;
        strong {
          font-weight: 700;
        }
      }
      .item-desc {
        flex: 65%;
        font-size: 0.875rem;
        font-weight: 200;
        margin: 0.1rem 0 0;
        padding: 0 5%;
        line-height: 1.5rem;
        a {
          color: #333;
          font-weight: 700;
          text-decoration: underline;
          transition: all 0.15s cubic-bezier(0.4, 0, 0, 1);
          &:hover {
            background: rgba(0, 0, 0, 0.85);
            color: #fff;
          }
        }
      }
    }
  }
}
</style>
