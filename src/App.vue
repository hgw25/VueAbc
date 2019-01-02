<template>
  <div id="app">
    <div v-if="false">
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
    <div>
      <ListPage v-if="true"></ListPage>
      <input
        v-model="testModel"
        placeholder="这是一个傻不拉几的输入框"
        @change="handelChange"
        @click="handelClick"
      >
      <div class="bg-red" :style="{'background-color': item.color}" v-for="(item, index) in bgList" :key="index">{{ item.name }}</div>
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
    return {
      testModel: "",
      bgList: [{name: '小猫', color: 'red'}, {name: '小狗', color: 'blue'}, {name: '小王', color: 'gold'}, {name: '小新', color: 'green'}]
    };
  },
  created() {
    console.log("我被创建啦");
    // this.name();
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
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.bg-red {
  height: 100px;
  width: 200px;
}
</style>
