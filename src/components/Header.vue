<!-- 头部公共菜单 -->
<template>
  <div class='wrap'>
      <div class="header-wrap">
          <p></p>
          <span>{{date}}</span>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      date: ''
    }
  },
  mounted(){
    setInterval(() => {
      this.getDate()
    }, 1000);
  },
  methods: {
    getDate(){
      this.date = new Date().toLocaleString()
    }
  }
}

</script>
<style lang='scss' scoped>
@keyframes bgp{
    0%{
        background-position: 0 0;
    }
    100%{
        background-position: -100% 0;
    }
}
.header-wrap{
    width: calc(100% - 64px);
    margin: 0 auto;
    padding: 0 32px;
    height: 40px;
    background:rgba(255, 255, 255, .7);
    user-select: none;
    @media screen and (max-width: 980px) {
      width: 100%;
    }
    p,span{
      background-image: linear-gradient(to right, red, orange, yellow, green, blue, green, yellow, orange, red, orange, yellow, green, blue, green, yellow, orange, red);    
      -webkit-text-fill-color: transparent;
      -webkit-background-clip: text;
      -webkit-background-size: 200% 100%;
      animation: bgp 5s infinite linear;
      line-height: 40px;
    }
    p{
      float: left;
    }
    span{
      float: right;
    }
}
</style>