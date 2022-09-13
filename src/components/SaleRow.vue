<template>
  <tr :style=classObject>
    <td>{{ id }}</td>
    <td>{{ article }}</td>
    <td style="text-align: left;">
      <div>
        <ul>
          <li v-for='r in items' :key='r.id'>{{ r.id }} - {{ r.item }}</li>
        </ul>
      </div>
    </td>
    <td >
      <img :src="imagen.source" :alt="imagen.descripcion" />
    </td>
  </tr>
</template>

<script>
export default {
  name: 'SaleRow',
  props: {
    article: String,
    id: Number,
    items: Array,
    imagen: {
      sourse: String,
      descripcion: String,
    },
    styleObject: {},
  },
  methods: {
    classObject1() {
      return this.id % 2 === 0
        ? 'background-color:white'
        : 'background-color:beige';
    },
  },
  computed: {
    classObject() {
      return this.id % 2 === 0
        ? 'background-color:white'
        : 'background-color:beige';
    },
  },
};
</script>

<style></style>
