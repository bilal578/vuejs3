<template>
<form @submit="storeUser">
  <input type="text" placeholder="Enter name" v-model="name"><br><br>
  <input type="text" placeholder="Enter email" v-model="email"><br><br>
  <!-- <input type="submit" value="Add User"> -->
 <Button>Add Users</Button>


 
</form>
</template>

<script>
 import Button from './Button'
export default {
    name:'AddUser',
    components:{
         Button,
    },
    data(){
        return{
            name:'',
            email:''
        }
    },
    methods:{
        storeUser:function(e){
                e.preventDefault();
                this.$emit("add-user",{name:this.name,email:this.email});
        }
    }

}
</script>

<style scoped>
input{
    padding: 10px;
    border-radius: 5px;
    border:1px solid black;
    text-align: center;
    
}
</style>

