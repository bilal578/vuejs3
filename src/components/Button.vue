<template>
  <button type="submit" class="button">
  <slot></slot>
  </button>
</template>

<script>
export default {
    name:'Button'

}
</script>

<style>
.button{
    background: red;
    color: #fff;
    border: none;
    border-radius: 3px;
    outline: none;
    padding:10px 15px;
    font-size: 15px;
}
</style>