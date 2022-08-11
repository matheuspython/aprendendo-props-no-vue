<template>
  <header>{{ title }}</header>
</template>
<script>
export default {
  name: "TheHeader",
  props: {
    title: {
      type: String,
      default: "bem vindo!",
    },
  },
};
</script>
<style scoped>
header {
  width: 100%;
  min-height: 45px;
  padding: 15px;
  background: #6b1ee9;
  color: #fff;
  align-items: center;
  display: flex;
  justify-content: center;
  font-size: 1.5rem;
}
</style>
