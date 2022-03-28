<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 ref="testH2">Essential Links{{ new Date() }}</h2>
    <button title="haha" @click="btnChange">按钮</button>

    <TestA ref="refTestA"></TestA>
  </div>
</template>

<script>
import TestA from "@/components/TestA";
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
  components: {
    TestA,
  },
  methods: {
    btnChange(e) {
      // 两种调用子组件中的属性和方法
      // 方法一
      console.log(this.$children[0].msg);
      this.$children[0].refresh();
      // 方法二
      console.log(e.target.msg);
      this.$refs.refTestA.refresh();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="" setup>
h2 {
  color: pink;
}
</style>