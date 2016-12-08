<template>
<div class="message">{{msg}}</div>
</template>
<script>
export default {
  data () {
   return {
    msg: 'Welcome to Vue World!'
    }
  }
}
</script>
<style>
.message{
   color:green;
   font-size:56px;
   font-weight:bold;
}
</style>