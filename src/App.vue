<template>
  <div>
 <form-page @data="uploadCard($event)"></form-page>
 <list-page   v-for="(i,index) in card" :key="index" :title="i[1]" :textarea="i[0]"  :url="i[2]"></list-page>
 
</div>
</template>

<script>
import FormPage from './components/FormPage'
import ListPage from './components/ListPage.vue'



export default {
  name: 'App',
  components:{
    FormPage,
    ListPage
    
   
  },
  data() {
    return {
      card:[]
    }
  },
  methods: {
    uploadCard(e){
      this.card.push(e)
      console.log(this.card)
    },

  },
  
}
</script>

<style>
div{
  margin:0 auto;
 width: 500px;


}
</style>
