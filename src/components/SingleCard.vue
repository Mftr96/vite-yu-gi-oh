<script>
import store from '../data/store.js';

export default{
 
  
  data (){
    //dati lo metto qui perchè non è un componente vue
    return{store,

    }
  },
  methods:{

  },
  mounted(){
    console.log("SingleCard montato")

  }
}

</script>

<template>
  <div class="card " v-for="card in store.dati" >      
    <img :src="card.card_images[0].image_url" alt="">
    <div class="info-card">
      <h3>{{card.name}}</h3>
      <p>{{card.archetype}}</p>
    </div>
  </div>
  
</template>

<style scoped>
.card{
  width: calc(800px / 5 - 1.5rem);
  border: 1px solid black;
  background-color: rgb(212, 143, 56) ;
  
}
h3{
  color: white;
}
h3,p{
  text-align: center;

}
.card img{
  width: 100%;
}
.card p{
  width: 100%;
}

</style>
