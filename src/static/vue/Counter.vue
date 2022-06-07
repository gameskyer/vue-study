<template>
  <div id="counter">
    Counter: {{ counter }}
  </div>
  <button @click="stop()">stop</button>
</template>
<script>
export default {
  data () {
    return {
      time: null,//用来存放定时器
      counter: 0,
    };
  },
  mounted () {
    this.time = setInterval(() => {
      this.counter++
    }, 1000)
  },
  methods: {
    stop () {
      console.log("调用了STOP")
      clearInterval(this.time)
    }
  }
};
</script>
