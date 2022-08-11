<template>
  <TheHeader title="seja bem vindo!!" />
  <main>
    <div class="additem">
      <input class="text"  placeholder="digite o texto aqui" type="text" v-model="texto">
      <input  class="text" placeholder="digite sua img aqui" type="text" v-model="img">
      <label> escolha uma cor abaixo </label>
      <input  class="color" type="color" v-model="cor">
      <button @click="addItem" type="button">adicionar</button>
    </div>
    <!-- <input type="color" v-model="cor" name="" id="" /> -->
    <div class="container">
      <Boxes
        v-for="(item, index) in list"
        :Key="index"
        :color="item.color"
        :text="item.text"
        :img="item.img"
      />
    </div>

  </main>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import Boxes from "./components/Boxes.vue";

export default {
  name: "App",
  data() {
    return {
      list: [
        {
          img: "http://github.com/naruto.png",
          color: "purple",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/goku.png",
          color: "red",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/vegeta.png",
          color: "blue",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/golang.png",
          color: "black",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/gate.png",
          color: "gray",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/python.png",
          color: "green",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/java.png",
          color: "yellow",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/javascript.png",
          color: "orange",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/reactjs.png",
          color: "gold",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
        {
          img: "http://github.com/vuejs.png",
          color: "brown",
          text: "lomreffdsa fasdfsda fsda fsdf sadf sadfasdf asdf asdf asdf",
        },
      ],
    };
  },
  methods: {
    addItem(){
      this.list.push({
        color: this.cor,
        img: this.img,
        text: this.texto,
      })
    }
  },
  components: {
    TheHeader,
    Boxes,
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html,
body {
  font-family: sans-serif;
}
#app {
  width: 100%;
}
.container{
  display: flex;
  margin: 0 auto;
  width: 100%;
  max-width: 1280px;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
.additem{
  margin: 15px auto;
  width: 300px;
  display: flex;
  flex-direction: column;
}

.additem .text{
  width: 95%;
  margin: 5px auto;
  border-radius: 15px;
  height: 35px;
  background: rgb(226, 222, 222);
  padding-left: 15px;
  border: 0;
}
.color{
   width: 95%;
  margin: 5px auto;
  height: 35px;
  background: transparent;
  border:0;
  border-radius: 15px;
  overflow: hidden;cursor: pointer;
}
.additem button{
   width: 95%;
  margin: 5px auto;
  height: 35px;
  border:0;
  background: rgb(155, 13, 238);
  border-radius: 15px;
 cursor: pointer;
 color: #fff;
}
label{
  text-align: center;
}
</style>
