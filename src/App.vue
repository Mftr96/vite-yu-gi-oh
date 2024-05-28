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
      searchType:"",

    }
  },
  methods:{
    f_bottone(){
      console.log(this.searchType)
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0&archetype='+this.searchType)
    .then((response)=>{
        const AxCardList=response.data.data;
        console.log(AxCardList);
        this.store.dati="";
        this.store.dati=AxCardList
    });

    },
    

    },
  mounted(){
    //funzione che svuota array all'avvio e pusha i dat ipresi dall'API
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
  <select v-model="searchType" name="archetype-select" id="select-name">
    <option v-for="archetipi in store.archetipi" :value="archetipi.archetype_name">
    {{archetipi.archetype_name}}
    </option>
  </select>
  <button @click="f_bottone()">bottone archetipo</button>
  <CardList/> 
</template>

<style scoped>
select{
  margin-left: 2rem;
}

</style>
