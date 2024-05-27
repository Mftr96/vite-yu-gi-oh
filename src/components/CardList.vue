<script>
import SingleCard from './SingleCard.vue'
import dati from '../data/store.js';

export default{

    components:{
        SingleCard,
        
    },
  data (){
    return{
      dati,
    }
  },
  methods:{

  },
  mounted(){
    console.log("CardList montato")

  }
}

</script>

<template>
  <!-- Raccoglitore carte -->
  <div class="container">
    
      <SingleCard/>
  
  </div>
    
</template>

<style scoped>
.container{
  width: 800px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  border: 1px solid crimson;
  background-color: white;
}

</style>
