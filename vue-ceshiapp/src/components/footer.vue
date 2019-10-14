<template>
  <footer v-on:click="changetitle">
    <p>{{copyright}}{{title}}</p>
  </footer>
</template>

<script>
export default {
  name: "app-footer",
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      copyright: "Copyright 2017 Vue Demo"
    };
  },
  methods: {
    changetitle: function() {
      //   this.title2 = "change";
      this.$emit("titleChange", "子项目向父传值");
    }
  }
  /*     beforeCreate:function() {
        alert('组件实例化之前执行的函数')
    },
    created:function() {
        alert('组件实例化完毕，但页面还未显示')
    },
    beforeMount:function(){
        alert('组件挂载前，页面仍未显示，但虚拟dom已经配置')
    },
    mounted:function(){
        alert('组件挂载后，此方法执行后，页面显示')
    },
    beforeUpdate:function() {
        alert('组件更新前，页面仍未显示，但虚拟dom已经配置')
    },
    updated:function() {
        alert('组件更新前，此方法执行后，页面显示')
    },
    beforeDestory:function(){
        alert('组件销毁前')
    },
    destoryed:function(){
        alert('组件销毁')
    }, */
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer {
  background: #222;
  padding: 10px;
}
p {
  color: lightgreen;
  text-align: center;
}
</style>