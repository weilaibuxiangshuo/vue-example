<template>
  <div id="home">
    <app-header v-bind:title="title"></app-header>
    <users v-bind:users="users"></users>
    <users v-bind:users="users"></users>
    <app-footer v-on:titleChange="updatetitle($event)" v-bind:title="title"></app-footer>
  </div>
</template>

<script>
//局注册组件
import Users from './users'
import Header from './header'
import Footer from './footer'
export default {
  name: 'home',
  data(){
    return {
      users:[
        //   {name:'heryy',position:'Web 开发',show:false},
        //   {name:'heryy',position:'Web 开发',show:false},
        //   {name:'heryy',position:'Web 开发',show:false},
        //   {name:'heryy',position:'Web 开发',show:false},
        //   {name:'heryy',position:'Web 开发',show:false},
        //   {name:'heryy',position:'Web 开发',show:false},
          ],
          title:"传递的是一个值，(number,boolean,string)"
    }
  },
  methods:{
    updatetitle:function(subtitle){
      this.title=subtitle
    }
  },
  components:{
    //两种方式都是可以的
    "users":Users,
    "app-header":Header,
    "app-footer":Footer,
    },
    created() {
        this.$http.get("http://jsonplaceholder.typicode.com/users")
        .then((data)=>{
            // console.log(data)
            this.users=data.body
        })
    },
}
</script>
<style scoped>
h1 {
  color:purple;
}
</style>
