<template>
  <div id="app">
    <div>
      <ListPage></ListPage>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ListPage from "./components/ListPage.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    ListPage
  },
  data() {
  },
  methods: {
    name() {
      alert();
    },
    handelChange() {
      console.log(this.testModel);
    },
    handelClick() {
      alert("这是一个点击事件" + this.testModel);
    }
  }
};
</script>

<style>
/* #app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
*{
  margin: 0px;
  padding: 0px;
}
body{
  background: #000;
}
</style>
