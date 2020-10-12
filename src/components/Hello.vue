<template>
    <div class="hello">
        <h1>{{homeTitle}}</h1>
        <p>this component created by Bilal Ahmed</p>
        <h4 v-for="(user,index) in allUsers" v-bind:key="index">
            {{user}}
        </h4>
        <button @click="callfunction"> click me</button>
    </div>
</template>
<script>
export default {
    name:"Hello",
    props:["homeTitle","allUsers"],
    data(){
        return{
            title:"This is my first VUE component"
        }
    },
    methods:{
        callfunction:function(){
            console.log('Hello world')
        }
    }
}
</script>

<style  scoped>

</style>