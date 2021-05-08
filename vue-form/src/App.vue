<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="text" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    submitForm: function() {
      console.log('username : ', this.username);
      console.log('password : ', this.password);

      var url = 'https://jsonplaceholder.typicode.com/users';
      var data = {
        username: this.username,
        password: this.password
      };

      axios.post(url, data)
      .then((res) => {
        console.log('response : ', res);
      })
      .catch((err) => {
        console.error('error : ', err);
      });
    }
  }
}
</script>

<style>

</style>