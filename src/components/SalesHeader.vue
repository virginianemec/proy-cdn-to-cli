<template>
  <div class="coder--header">
    <h1>{{ title }} - {{ presentation_name }}</h1>
    <div class='descripcion' v-html="workDescription"></div>
  </div>
</template>

<script>
export default {
  name: 'SalesHeader',
  data() {
    return {
      title: 'Hello Coderhouse!',
      presentation_name: 'Mi nombre es Virginia Nemec',
      workDescription: `DESAFIO DE VUE CDN A VUE CLI <br>
Convierte tu desafío de la Clase 04 de Vue CDN a Vue Cli. `,
    };
  },
};
</script>

<style >
.coder--header {
  background-color: #393B43;
}
h1 {
  color: #E5F876;
  font-size: 25px;
  padding: 10px;
}
.descripcion {
  background-color: #E5F876;
  color: black;
  padding: 10px;
  }

</style>
