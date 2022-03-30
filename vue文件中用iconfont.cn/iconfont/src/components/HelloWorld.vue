<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <a-icon type="step-backward" />
    <icon-font type="icon-query1" />
    <icon-font type="icon-24gl-playlistVideo" />
    <icon-font type="icon-sousuowenjian"></icon-font>
    <icon-font type="icon-liebiaoshitucaidan"></icon-font>
  </div>
</template>

<script>
import { Icon } from 'ant-design-vue';

const IconFont = Icon.createFromIconfontCN({
  scriptUrl: '//at.alicdn.com/t/font_3219925_9zj8aicgslt.js',
});

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
  components: {
    IconFont,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
