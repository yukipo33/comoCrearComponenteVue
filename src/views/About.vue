<template>
  <div class="about">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>This is the second Table</h1>
    <div class="tabla">
    <Tabla :titulos="tanjiro" :datos="zenitsu"></Tabla>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src
import Tabla from "@/components/Tabla.vue";

export default {
  name: "about",
  components: {
    Tabla
  },
  data: () => {
    return {
      tanjiro: [
        // {
        //   company: "x",
        //   contact: "y",
        //   country: "z"
        // }
        {
          company: "Company",
          contact: "Contact",
          country: "Country"
        }
      ],
      zenitsu: [
        { company: "Powerade", contact: "Jade", country: "Mexico" },
        { company: "Apple", contact: "jobs", country: "USA" },
        { company: "Samsung", contact: "Lee Jong Suk", country: "South Corea" }
      ]
    };
  }
};
</script>
<style scoped>
  .tabla{
    width: 100%;
    /* border: 2px solid green; */
    display: flex;
    justify-content: center;
  }
  .about{
    height: 82vh;
  }
</style>
