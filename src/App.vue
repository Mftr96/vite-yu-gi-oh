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
    return{dati

    }
  },
  methods:{

  },
  mounted(){
    //funzione che svuota array all'avvio e pusha i dat ipresi dall'API
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0')
    .then((response)=>{
        const AxCardList=response.data;
        console.log(AxCardList);
        this.card=[];
        this.card.push(AxCardList)
        console.log(this.card);
    })
  }
}
</script>

<template>
  <h1>Yugi-oh API</h1>
  <CardList/>
  
  
</template>

<style scoped>

</style>
