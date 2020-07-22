<template>
  <div class="part-one">
    <img
      class="part-one-image"
      :src="headImage"
      alt="头像"
    >
    <p>姓&emsp;&emsp;名：陈宇</p>
    <p>学&emsp;&emsp;历：本科</p>
    <p>工作年限：3 年</p>
    <p>年&emsp;&emsp;龄：25</p>
    <p>联系电话：18883269663</p>
    <p>电子邮箱：chenyu@mydearest.cn</p>
    <p>博&emsp;&emsp;客：<a
        href="https://mydearest.cn"
        target="_blank"
      >mydearest.cn</a></p>
    <p>掘&emsp;&emsp;金：<a
        href="https://juejin.im/user/5a59acf9518825733422a857"
        target="_blank"
      >cosyer</a></p>
    <p>GitHub：<a
        href="https://github.com/cosyer"
        target="_blank"
      >cosyer</a></p>
  </div>
</template>

<script>
export default {
  name: "partOne",
  data() {
    return {
      headImage: require("../assets/img/head_image.png")
    };
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
p {
  line-height: 30px;
}
.part-one {
  width: 100%;
  height: 500px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
  padding-left: 10px;
}
.part-one-image {
  width: 150px;
  height: 150px;
}
</style>