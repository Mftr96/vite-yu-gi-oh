<script >
//importo i componenti  e dati(dati lo prendo da store.js)
import CardList from './components/CardList.vue';
import SingleCard from './components/SingleCard.vue';
import dati from './data/store.js';
//esporto questi dati nell'HTML
export default{
  components:{
    CardList,
    SingleCard,
  },
  data (){
    return{

    }
  },
  methods:{

  },
  mounted(){

  }
}
</script>

<template>
  <h1>Yugi-oh API</h1>
  <CardList/>
  
  
</template>

<style scoped>

</style>
