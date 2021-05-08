<template>
  <!-- For HTML -->
  <div>
    <app-header></app-header>
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
      str: 'kyomin'
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