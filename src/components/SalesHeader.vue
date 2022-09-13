<template>
  <div class="coder--header">
    <h1>{{ title }} - {{ presentacion_name }}</h1>
    <div class='descripcion'>{{ workDescription }}</div>
  </div>
</template>

<script>
export default {
  name: 'SalesHeader',
  data() {
    return {
      title: 'Hello Coderhouse!',
      presentacion_name: 'Mi nombre es Virginia Nemec',
      workDescription: 'Desafío: Proyecto 2',
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
