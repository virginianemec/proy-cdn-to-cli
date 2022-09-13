<template>
  <div>
    <div class='titulo'>{{ title }} - {{ presentacion_name }}</div>
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
      workDescription: 'Desafio: Proyeto 2',
    };
  },
};
</script>

<style></style>
