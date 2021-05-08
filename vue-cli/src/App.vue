<template>
  <!-- For HTML -->
  <div>
    <!-- 
      하위 컴포넌트에 props 전달 방식
      <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> 
    -->
    <app-header v-bind:propsdata="str"></app-header>
  </div>
</template>

<script>
// 기존
// var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }
import AppHeader from './components/AppHeader.vue';

// 기존
// new Vue({
//   data: {
//     str: 'kyomin'
//   }
// });
export default {
  data: function() {
    return {
      str: 'Kyomin'
    }
  },
  components: {
    'app-header': AppHeader
  }
}
</script>

<style>
  /* For CSS */
</style>