<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Tabla :estilo="tablaStyle" :titulos="inosuke" :datos="nezuko"></Tabla>
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
        {
          company: "a",
          contact: "b",
          country: "c"
        }
      ],
      nezuko: [
        { company: "gatorade", contact: "magaly", country: "mexico" },
        { company: "jumex", contact: "raul", country: "suecia" },
        { company: "dell", contact: "steve", country: "noruega" }
      ],
      tablaStyle: "tablaBlue"
    };
  }
};
/*

'gatorade','magaly','mexico'


{"company":"gatorade","contact": "magaly","country": "mexico"},
{"company":"jumex","contact": "raul","country": "suecia"},
{"company":"dell","contact": "steve","country": "noruega"}

{company:"gatorade",contact: "magaly",country: "mexico"},
{company:"jumex",contact: "raul",country: "suecia"},
{company:"dell", contact: "steve",country: "noruega"}


{company:'gatorade',contact: 'magaly',country: 'mexico'},
{company:'jumex',contact: 'raul',country: 'suecia'},
{company:'dell', contact: 'steve',country: 'noruega'}


'{"company":"gatorade","contact": "magaly","country": "mexico"}',
'{"company":"jumex","contact": "raul","country": "suecia"}',
'{"company":"dell","contact": "steve","country": "noruega"}'

*/
</script>
