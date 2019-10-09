<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="First Table"/>
    <div class="tabla">
      <Tabla :estilo="tablaStyle" :titulos="inosuke" :datos="nezuko"></Tabla>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Tabla from "@/components/Tabla.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    Tabla
  },
  data: () => {
    return {
      inosuke: [
        // {
        //   company: "a",
        //   contact: "b",
        //   country: "c"
        // }
        {
          company: "Company",
          contact: "Contact",
          country: "Country"
        }
      ],
      nezuko: [
        { company: "Gatorade", contact: "Magaly", country: "Mexico" },
        { company: "Jumex", contact: "Raul", country: "Mexico" },
        { company: "Xiaomi", contact: "Steve", country: "China" }
      ],
      tablaStyle: "tablaBlue"
    };
  }
};

</script>

<style scoped>
  .tabla{
    width: 100%;
    /* border: 2px solid pink; */
    display: flex;
    justify-content: center;
  }
  .home{
    height: 82vh;
  }

</style>
