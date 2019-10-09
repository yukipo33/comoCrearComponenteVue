<template>
  <div>
    <table :class="estilo">
      <tr v-for="nuevosTitulos in titulos" :key="nuevosTitulos.id">
        <th>{{nuevosTitulos.company}}</th>
        <th>{{nuevosTitulos.contact}}</th>
        <th>{{nuevosTitulos.country}}</th>
      </tr>
      <tr v-for="nuevosDatos in datos" :key="nuevosDatos.id">
        <!-- <td>{{nuevosDatos}}</td> -->
        <td>{{nuevosDatos.company}}</td>
        <td>{{nuevosDatos.contact}}</td>
        <td>{{nuevosDatos.country}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "tabla",
  props: {
    titulos: {
      type: Array,
      default: function() {
        return [];
      }
    },
    datos: {
      type: Array,
      default: function() {
        return [];
      }
    },
    estilo: {
      type: String,
      default: function() {
        return "tablaRed";
      }
    }
  }
};
</script>

<style>
table {
  border: 1px solid;
}
td, th {
  border: 1px solid;
}

.tablaRed{
  border-color: red;
  font-weight: bold;
}
.tablaBlue{
  border-color: blue;
  font-size: 36px;
}

</style>
