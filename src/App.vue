<template>
  <div id="app">
    <Header />
    <div class="content">
      <div class="con-sL animate__animated animate__fadeInLeft">
        <personal-info />
        <catalog />
      </div>
      <div class="con-sM animate__animated animate__fadeInUp">
        <router-view />
      </div>
      <div class="con-sR animate__animated animate__fadeInRight"></div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import PersonalInfo from "./components/PersonalInfo";
import Catalog from "./components/Catalog"
export default {
  data() {
    return {};
  },
  components: {
    Header,
    PersonalInfo,
    Catalog
  },
};
</script>

<style lang='scss'>
.content{
  margin-top: 10px;
  padding: 0 32px;
  height: calc(100% - 50px);
  &::after{
    content: "";
    display: block;
    clear: both;
  }
  .con-sL{
    margin-right: 10px;
    float: left;
  }
  .con-sM{
    width: 980px;
    height: 100%;
    float: left;
  }
  .con-sR{
    float: right;
    width: 300px;
    margin-left: 10px;
    min-height: 500px;
    background: rgba(255, 255, 255, .7);
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
