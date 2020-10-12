<template>
<!-- <Hello v-bind:homeTitle=" homeTitle" :allUsers="user" /> -->
<h1>Vue Js</h1>
<AddUser @add-user="storeUser"/>
<Show :users="users"/>
</template>

<script>
// import Hello from "./components/Hello"
import AddUser from './components/AddUser';
import Show from './components/Show';
import axios from 'axios';
// import Button from './components/Button'
export default {
  
  name: 'App',
  components: {
    AddUser,
    Show,
    
  },
  data(){
    return{
    homeTitle:"hello my first vue cli app component",
    users:[],
  };
  },
  methods:{
    storeUser:function(user){
      this.users=[user,...this.users]
    }
  },
  async created(){
    try {
      const response = await axios.get(
      "https://jsonplaceholder.typicode.com/posts");
      console.log(response.data);
      
    } catch (error) {
      console.log(error);
    }
  }
}
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
