<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Tabla :titulos="tanjiro" :datos="zenitsu"></Tabla>
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
        {
          company: "x",
          contact: "y",
          country: "z"
        }
      ],
      zenitsu: [
        { company: "powerade", contact: "magaly", country: "mexico" },
        { company: "apple", contact: "jobs", country: "USA" },
        { company: "mafia", contact: "corleone", country: "italia" }
      ]
    };
  }
};
</script>
