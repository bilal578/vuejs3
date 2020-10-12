<template>
  <div class="show"></div>
  <h4 v-for="(user, index) in users" :key="index">
      {{user.name}} == {{user.email}}
  </h4>
</template>

<script>
export default {
name:"Show",
props:["users"],
}
</script>

<style>

</style>