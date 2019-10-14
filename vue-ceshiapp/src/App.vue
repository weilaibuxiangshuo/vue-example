<template>
  <div id="app">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/helloworld">HelloWorld</router-link></li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>
//局注册组件
import Users from './components/users'
import Header from './components/header'
import Footer from './components/footer'
export default {
  name: 'App',
  data(){
    return {
      msg:""
    }
  }
}
</script>
<style scoped>
h1 {
  color:purple;
}
</style>
