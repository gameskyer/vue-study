<template>
  <div id="chart" style="width:800px;height:400px;"></div>
</template>
<script lang="ts">
// eslint-disable-next-line no-unused-vars
// import { Options, Vue } from "vue-class-component";
// import * as echarts from "echarts";
// window.onload = function () {
//   console.log("2222222222222222");
//   const option = {
//     title: {
//       text: "堆叠区域图",
//     },
//     tooltip: {
//       trigger: "axis",
//       axisPointer: {
//         type: "cross",
//         label: {
//           backgroundColor: "#6a7985",
//         },
//       },
//     },
//     legend: {
//       data: ["邮件营销", "联盟广告", "视频广告", "直接访问", "搜索引擎"],
//     },
//     toolbox: {
//       feature: {
//         saveAsImage: {},
//       },
//     },
//     grid: {
//       left: "3%",
//       right: "4%",
//       bottom: "3%",
//       containLabel: true,
//     },
//     xAxis: [
//       {
//         type: "category",
//         boundaryGap: false,
//         data: ["周一", "周二", "周三", "周四", "周五", "周六", "周日"],
//       },
//     ],
//     yAxis: [
//       {
//         type: "value",
//       },
//     ],
//     series: [
//       {
//         name: "邮件营销",
//         type: "line",
//         stack: "总量",
//         areaStyle: {},
//         data: [120, 132, 101, 134, 90, 230, 210],
//       },
//       {
//         name: "联盟广告",
//         type: "line",
//         stack: "总量",
//         areaStyle: {},
//         data: [220, 182, 191, 234, 290, 330, 310],
//       },
//       {
//         name: "视频广告",
//         type: "line",
//         stack: "总量",
//         areaStyle: {},
//         data: [150, 232, 201, 154, 190, 330, 410],
//       },
//       {
//         name: "直接访问",
//         type: "line",
//         stack: "总量",
//         areaStyle: {},
//         data: [320, 332, 301, 334, 390, 330, 320],
//       },
//       {
//         name: "搜索引擎",
//         type: "line",
//         stack: "总量",
//         label: {
//           normal: {
//             show: true,
//             position: "top",
//           },
//         },
//         areaStyle: {},
//         data: [820, 932, 901, 934, 1290, 1330, 1320],
//       },
//     ],
//   };
//   const chart = echarts.init(
//     document.getElementById("chart") as HTMLDivElement
//   );
//   chart.setOption(option);
// };

import { Vue } from "vue-class-component";
import * as echarts from "echarts";
window.onload = function () {
  const myChart = echarts.init(
    document.getElementById("chart") as HTMLDivElement
  );
  type EChartsOption = echarts.EChartsOption;
  var option: EChartsOption;
  option = {
    title: {
      text: "多层次折线图",
    },
    tooltip: {
      trigger: "axis",
      axisPointer: {
        type: "cross",

        label: {
          backgroundColor: "#6a7985",
        },
      },
    },
    legend: {
      data: ["Email", "Union Ads", "Video Ads", "Direct", "Search Engine"],
    },
    toolbox: {
      feature: {
        saveAsImage: {},
      },
    },
    grid: {
      left: "3%",
      right: "4%",
      bottom: "3%",
      containLabel: true,
    },
    xAxis: [
      {
        type: "category",
        boundaryGap: false,
        data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"],
      },
    ],
    yAxis: [
      {
        type: "value",
      },
    ],
    series: [
      {
        name: "Email",
        type: "line",
        stack: "Total",
        areaStyle: {},
        emphasis: {
          focus: "series",
        },
        data: [1220, 132, 101, 134, 90, 230, 210],
      },
      {
        name: "Union Ads",
        type: "line",
        stack: "Total",
        areaStyle: {},
        emphasis: {
          focus: "series",
        },
        data: [220, 182, 191, 234, 290, 330, 310],
      },
      {
        name: "Video Ads",
        type: "line",
        stack: "Total",
        areaStyle: {},
        emphasis: {
          focus: "series",
        },
        data: [150, 232, 201, 154, 190, 330, 410],
      },
      {
        name: "Direct",
        type: "line",
        stack: "Total",
        areaStyle: {},
        emphasis: {
          focus: "series",
        },
        data: [320, 332, 301, 334, 390, 330, 320],
      },
      {
        name: "Search Engine",
        type: "line",
        stack: "Total",
        label: {
          show: true,
          position: "top",
        },
        areaStyle: {},
        emphasis: {
          focus: "series",
        },
        data: [820, 932, 901, 934, 1290, 1330, 1320],
      },
    ],
  };

  option && myChart.setOption(option);
};
export default class Echarts extends Vue {}
</script>