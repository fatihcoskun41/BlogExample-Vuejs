<template>

   <div>
   <h4>{{title}}</h4>


    <b-card-group  deck>
      <b-card>
          <img style="height: 300px; width:95%" :src="url">
        <b-card-text>
         {{textarea}}
        </b-card-text>
      
</b-card>
     
    </b-card-group>
    <br>
  </div>
</template>

<script>
export default {
    data() {
        return {
        
        
        }
    },
    props:["title","textarea","url"]


    

}
</script>

<style>

</style>