<template>
  <div class="coder--header">
    <h1>{{ title }} - {{ presentation_name }}</h1>
    <div class='descripcion'>{{ workDescription }}</div>
  </div>
</template>

<script>
export default {
  name: 'SalesHeader',
  data() {
    return {
      title: 'Hello Coderhouse!',
      presentation_name: 'Mi nombre es Virginia Nemec',
      workDescription: 'Desafío 3: Proyecto02 -> de CDN a CLI',
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
