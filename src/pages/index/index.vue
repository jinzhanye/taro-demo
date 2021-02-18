<template>
  <view class="index" ref="hello"
        @tap="onClick">
    <NumberDisplay/>
    <NumberSubmit/>
  </view>
</template>

<script>
import NumberDisplay from '../../components/NumberDisplay.vue'
import NumberSubmit from '../../components/NumberSubmit.vue'

export default {
  name: 'Index',
  components: {
    NumberDisplay,
    NumberSubmit
  },
  onShareAppMessage() {
    return {
      title: '自定义标题',
      imageUrl: 'http://demo.png',
      query: 'name=xxx&age=xxx',
    }
  },
  methods: {
    onClick() {
      console.log('123123')
    }
  },
  mounted() {
    const dom = this.$refs.hello
    console.dir(dom)
    dom.setAttribute('style', 'background: red')


    debugger
    window.addEventListener('click',() => {
      console.log('hello')
    })
  }
}
</script>

<style>
.index {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
