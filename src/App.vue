<script>
//importo i componenti  e dati(dati lo prendo da store.js)
import CardList from './components/CardList.vue';
import store from './data/store.js';
import axios from 'axios';
//esporto questi dati nell'HTML
export default{
  components:{
    CardList,
    
  },
  data (){
    return{store,

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
    });
    //funzione che alla chiamata resituisce array con archetipi
    axios.get("https://db.ygoprodeck.com/api/v7/archetypes.php")
    .then((response)=>{
      const ArcheList=response.data
      console.log(ArcheList)
      this.store.archetipi=ArcheList
    });
    console.log(this.store.archetipi)

  }
}
</script>

<template>
  <h1>Yugi-oh API</h1>
  <select name="archetype-select" id="select-name">
    <option v-for="archetipi in store.archetipi" value="">
    {{archetipi.archetype_name}}
    </option>
  </select>
  <button @click="">bottone archetipo</button>
  <CardList/> 
</template>

<style scoped>
select{
  margin-left: 2rem;
}

</style>
