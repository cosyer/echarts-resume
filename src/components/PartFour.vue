<template>
  <div
    :class="partFour"
    id="part-four"
  ></div>
</template>

<script>
// 引入基本模板
let echarts = require("echarts/lib/echarts");

export default {
  name: "partFour",
  data() {
    return {
      partFour: "part-four",
      curWidth: 0,
    };
  },
  beforeMount() {
    this.curWidth =
      document.documentElement.clientWidth || document.body.clientWidth;
    if (this.curWidth < 1600) {
      this.partFour = "part-four-responsive";
    }
  },
  mounted() {
    this.drawECharts();
  },
  methods: {
    drawECharts() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = echarts.init(document.getElementById("part-four"));

      myChart.setOption({
        // 标题
        title: {
          // 标题文本
          text: "文章成就统计",
          // 标题文本样式
          textStyle: {
            color: "#fff",
          },
          // 标题位置
          x: "center",
        },
        // 图形布局
        grid: {
          // 距离底部高度
          bottom: "20",
        },
        // 横轴
        xAxis: {
          show: false,
          type: "category",
          data: [
            "Github 提交：\n627",
            "Github Star数：\n77",
            "博客文章数：\n147",
            "博客总字数：\n294.9k",
          ],
          axisLine: {
            lineStyle: {
              color: "#fff",
            },
          },
          axisLabel: {
            // 横轴信息全部显示
            interval: 0,
          },
        },
        // 纵轴
        yAxis: {
          type: "value",
          axisLine: {
            lineStyle: {
              color: "#fff",
            },
          },
          axisLabel: {
            // 横轴信息全部显示
            interval: 0,
          },
        },
        // 图形系列
        series: [
          {
            // 图类型
            type: "bar",
            // 数据
            data: [627, 77, 147, 294.9],
            // 文本
            label: {
              show: true,
              position: "top",
              color: "#fff",
              formatter: "{b}",
            },
            // 柱条样式
            itemStyle: {
              color: "deepskyblue",
            },
            zlevel: 1,
          },
        ],
      });
    },
  },
};
</script>

<style scoped>
.part-four {
  width: 100%;
  height: 310px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
.part-four-responsive {
  width: 100%;
  height: 400px;
  border: 5px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
</style>