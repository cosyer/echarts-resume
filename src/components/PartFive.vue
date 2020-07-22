<template>
  <div :class="partFive">
    <h3 class="text-center text-top">工作经验</h3>
    <p>
      <a
        href="http://www.aminfo.com.cn/"
        target="_blank"
      >南京富士通南大软件技术有限公司</a>
      <span class="text-small">| 2018 年 9 月—至今</span>
    </p>
    <p class="text-small">工作内容：</p>
    <p class="text-small">&emsp;1. 负责公司官网页面的重构和维护；</p>
    <p class="text-small">&emsp;2. 搭建项目架构，前后台分离开发。同时编写后台接口填补页面交互逻辑；</p>
    <p class="text-small">&emsp;3. 学习了开发基础知识和规范的项目流程，实现了从新人到 IT 入门的转变。</p>
    <p>
      <a
        href="https://www.qianmi.com/"
        target="_blank"
      >江苏千米网络科技股份有限公司</a>
      <span class="text-small">| 2017 年 8 月—2017 年 8 月</span>
    </p>
    <p class="text-small">工作内容：</p>
    <p class="text-small">&emsp;1. 负责公司官网页面的重构和维护；</p>
    <p class="text-small">&emsp;2. 搭建项目架构，前后台分离开发。同时编写后台接口填补页面交互逻辑；</p>
    <p class="text-small">&emsp;3. 学习了开发基础知识和规范的项目流程，实现了从新人到 IT 入门的转变。</p>
    <p>
      <a
        href="http://www.aminfo.com.cn/"
        target="_blank"
      >重庆新媒农信科技有限公司(实习)</a>
      <span class="text-small">| 2016 年 6 月—2017 年 7 月</span>
    </p>
    <p class="text-small">工作内容：</p>
    <p class="text-small">&emsp;1. 负责公司官网页面的重构和维护；</p>
    <p class="text-small">&emsp;2. 搭建项目架构，前后台分离开发。同时编写后台接口填补页面交互逻辑；</p>
    <p class="text-small">&emsp;3. 学习了开发基础知识和规范的项目流程，实现了从新人到 IT 入门的转变。</p>
  </div>
</template>

<script>
export default {
  name: "partFive",
  data() {
    return {
      partFive: "part-five",
      curWidth: 0
    };
  },
  beforeMount() {
    this.curWidth =
      document.documentElement.clientWidth || document.body.clientWidth;
    if (this.curWidth < 1600) {
      this.partFive = "part-five-responsive";
    }
  }
};
</script>

<style scoped>
a {
  color: deepskyblue;
}
a:hover {
  color: rgb(118, 190, 248);
}
.part-five {
  width: 100%;
  height: 310px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
  overflow: scroll;
}
.part-five-responsive {
  width: 100%;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
.text-center {
  text-align: center;
}
.text-small {
  font-size: 0.9em;
  color: rgb(253, 239, 239);
}
</style>