<template>
  <div :class="classDiv">
    <h1>{{msg}}</h1>
    <h2>{{inputText}}</h2>
    <h2 v-text="textoVText"></h2>
    <p v-html="textVHtml"></p>
    <input type="text" v-model="inputText">
    <img :src="img" alt="">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      inputText:"text from input",
      textoVText:"build-in directive v-text",
      textVHtml:'<a href="https://github.com/JuanCamiloMartinezLopez/Curso-Vue.git">repositorio del curso JuanCamiloMartinezLopez</a>',
      img:'https://picsum.photos/200/300',
      classDiv:'class_blue'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.class_blue{
  background-color: blue;
  color:black;
}
.class_red{
  background-color: red;
  color:white;
}
</style>
