<template>
<div class="box" :style="{background: color}">
    <img :src="img" :alt="text">
    <p>{{text}}</p>
</div>
</template>

<script>
export default {
    name: 'BoxVue',
    props:{
        text: String,
        color: String,
        img: String
    }
}
</script>

<style scoped>
    .box{
        width: 100%;
        max-width: 300px;
        padding: 15px;
        margin: 5px;
        border-radius: 15px;
    }
    .box img{
          width: 100%;
    }
    .box p {
        color: #fff;
        text-align: center;
    }
</style>