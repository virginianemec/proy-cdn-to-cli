<template>
  <div class="div--container">
     <table class="table border-primary">
        <thead>
          <tr>
            <th>ID</th>
            <th>NOMBRE</th>
            <th>ITEMS</th>
            <th>IMAGEN</th>
          </tr>
        </thead>
        <tbody v-for="sale in salesArray" :key="sale.id">
          <tr
            is="SaleRow"
            :id="sale.id"
            :article="sale.article"
            :items="sale.items"
            :imagen="sale.imagen"
            :style-object="sale.styleObject"
          ></tr>
        </tbody>
      </table>
    </div>
</template>

<script>
import SaleRow from './SaleRow.vue';

export default {
  name: 'SalesTable',
  components: {
    SaleRow,
  },
  data() {
    return {
      salesArray: [
        {
          id: 1,
          article: 'Verduleria',
          items: [
            { id: 1, item: 'Papa' },
            { id: 2, item: 'Pimiento' },
          ],
          imagen: {
            source: './imagenes/verduleria.jpg',
            descripcion: 'La Verduleria del barrio.',
          },
          styleObject: {
            background: '#59af6c',
          },
        },
        {
          id: 2,
          article: 'Panaderia',
          items: [],
          imagen: {
            source: './imagenes/panaderia.jpg',
            descripcion: 'La Panaderia del barrio.',
          },
          styleObject: {
            background: '#ffc107',
          },
        },
        {
          id: 3,
          article: 'Carniceria',
          items: [
            { id: 1, item: 'Costeleta' },
            { id: 2, item: 'Bife' },
          ],
          imagen: {
            source: './imagenes/carniceria.jpg',
            descripcion: 'La Carniceria del barrio.',
          },
          styleObject: {
            background: 'red',
          },
        },
      ],
      columns: [
        { id: 1, name: 'ID' },
        { id: 2, name: 'NOMBRE' },
        { id: 3, name: 'PRODUCTOS' },
        { id: 4, name: 'IMAGEN' },
      ],
    };
  },
  methods: {},
  computed: {},
};
</script>

<style scoped>
  .div--container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  gap: 10px;
  width: 100%;
  padding-top: 20px;
}
table {
  width: 80%;
  margin: auto;
  padding: 25px;
  margin-bottom: 20px;
  border-radius: 15px;
  box-shadow: 2px 2px 10px rgb(142, 142, 142);
  transition: 0.3s;
  color: #2c3e50;
  text-align: left;
}
</style>
