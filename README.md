# vue-mint-ui-example


## 1. ���̳�ʼ��

```
npm install -g vue-cli
vue init webpack vue-mint-ui-example
cd vue-mint-ui-example
npm install
npm run dev
```

��װ mint ui

```
npm install mint-ui -S
```


## 2. �������

main.js

``` js
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'
import router from './router'
import MintUI from 'mint-ui'
// ������ʽ
import 'mint-ui/lib/style.css'

Vue.config.productionTip = false
Vue.use(MintUI)

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  components: { App },
  template: '<App/>'
})

```

�޸� src\components\HelloWorld.vue

``` html
<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <mt-button @click.native="handleClick">��ť</mt-button>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    handleClick () {
      this.$toast('Hello world!');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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

```