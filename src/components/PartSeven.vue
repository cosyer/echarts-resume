<template>
  <div :class="partSeven">
    <h3 class="text-center">求职意向</h3>
    <p class="text-small"><span class="font-bold">期望职位：</span>前端工程师</p>
    <p class="text-small"><span class="font-bold">工作技能：</span>React全家桶、Vue全家桶</p>
    <p class="text-small"><span class="font-bold">目标城市：</span>南京、上海</p>
    <p class="text-small"><span class="font-bold">期望薪资：</span>15K - 20K</p>
    <p class="text-small"><span class="font-bold">入职时间：</span>在职考虑机会</p>
  </div>
</template>

<script>
export default {
  name: "partSeven",
  data() {
    return {
      partSeven: "part-seven",
      curWidth: 0,
    };
  },
  beforeMount() {
    this.curWidth =
      document.documentElement.clientWidth || document.body.clientWidth;
    if (this.curWidth < 1600) {
      this.partSeven = "part-sevev-responsive";
    }
  },
};
</script>

<style scoped>
.part-seven {
  width: 100%;
  height: 310px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
.part-sevev-responsive {
  width: 100%;
  height: 400px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
  overflow: scroll;
}
.text-center {
  text-align: center;
}
.text-small {
  font-size: 0.9em;
}
.font-bold {
  text-align: center;
  color: deepskyblue;
}
</style>