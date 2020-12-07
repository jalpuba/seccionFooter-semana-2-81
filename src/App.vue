<template>
  <div id="app">
    <seccion-api></seccion-api>
    <div class="container-fluid">
        <div class="row justify-content-center mb-5">
          <div class="col mt-5" v-for="(item,index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
          </div>
        </div>
    </div>    
    <seccion-footer></seccion-footer>
  </div>
</template>

<script>
import SeccionFooter from './components/SeccionFooter'
import TeamCard from './components/TeamCard.vue'
import SeccionApi from './components/SeccionApi'



export default {
  name: 'App',
  components:{
    SeccionFooter,
    TeamCard,
    SeccionApi
  },

  data(){
    return{
      team:[
        {
          codigo:1,
          nombre: "Luis",
          descripcion: "Sin informacion de gustos",
          rol:"Desarrollador backend",
          imagen: "https://placeimg.com/192/192/people",
        },
        {
          codigo:2,
          nombre: "Angélica",
          descripcion: "Le gusta jugar y no recuerdo más",
          rol:"Desarrollador backend",
          imagen: "https://placeimg.com/192/192/people",
        },
        {
          codigo:1,
          nombre: "Mauro",
          descripcion: "sueña con ser un sombrero blanco",
          rol:"Desarrollador backend",
          imagen: "https://placeimg.com/192/192/people",
        },
        {
          codigo:1,
          nombre: "Diana",
          descripcion: "la pola y la bici",
          rol:"Desarrollador backend",
          imagen: "https://placeimg.com/192/192/people",
        },
        {
          codigo:1,
          nombre: "James",
          descripcion: "videojuegos, musica",
          rol:"Desarrollador backend",
          imagen: "https://placeimg.com/192/192/people",
        }
      ]
    }
  }
}
</script>

