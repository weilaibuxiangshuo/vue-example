<template>
  <header v-on:click="changetitle" v-model="title2">
    <h1>{{title1}}{{title2}}</h1>
  </header>
</template>

<script>
export default {
  name: "app-header",
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      title2: this.title,
      title1: "vue.js demo"
    };
  },
  methods: {
    changetitle: function() {
      this.title2 = "change";
    }
  },
  /* beforeCreate: function() {
    alert("组件实例化之前执行的函数");
  },
  created: function() {
    alert("组件实例化完毕，但页面还未显示");
  },
  beforeMount: function() {
    alert("组件挂载前，页面仍未显示，但虚拟dom已经配置");
  },
  mounted: function() {
    alert("组件挂载后，此方法执行后，页面显示");
  },
  beforeUpdate: function() {
    alert("组件更新前，页面仍未显示，但虚拟dom已经配置");
  },
  updated: function() {
    alert("组件更新前，此方法执行后，页面显示");
  },
  beforeDestory: function() {
    alert("组件销毁前");
  },
  destoryed: function() {
    alert("组件销毁");
  } */
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  background: lightgreen;
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>