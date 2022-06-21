<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- 컴포넌트 명명법 종류 -->
    <!-- <helloWorld></hello-world>
    <HelloWorld></HelloWorld>
    <HelloWorld/> -->

    <div>
      <!-- <app-header v-bind: 프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
      <app-header v-bind:props="str" v-on:renew="renewStr"></app-header>
      {{ str }}
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import AppHeader from './components/AppHeader.vue'
//import AppHeader from '../../learn-vue-js-master/learn-vue-js-master/vue-cli-complete/src/components/AppHeader.vue'

// var appContent = {
//   props: ['propsdata']
// }

// var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }

//형식
export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  }, 
  methods: {
    renewStr: function() {
      this.str = 'hi';
    }
  }
}

// export default {
//   //인스턴스 옵션 속성 또는 컴포넌트 옵션 속성
//   name: 'App',
//   components: {
//     HelloWorld,
//     'hello-world' : HelloWorld,
//   }
// }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
