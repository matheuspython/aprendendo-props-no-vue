<template>
  <TheHeader title="seja bem vindo!!"/>
</template>

<script>
import TheHeader from './components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    TheHeader
}
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html, body{
  font-family: sans-serif;
}
#app {
  width: 100%;
}

</style>
