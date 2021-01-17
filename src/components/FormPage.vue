<template>
  <div>
    <b-form @submit="onSubmit" v-if="show">
      <b-form-group id="input-group-2"  label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="title"
          placeholder="Enter title"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group>
        <b-form-textarea
          id="textarea"
          v-model="textarea"
          placeholder="Enter something..."
          rows="3"
          max-rows="6"
        ></b-form-textarea>
      </b-form-group>
      <b-form-group>
        <b-form-input v-model="imageUrl" placeholder="Resim Linkini Giriniz"></b-form-input>
      </b-form-group>
     

      <b-button type="submit" variant="primary">Kaydet</b-button>
    </b-form>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      
        textarea: "",
        title: "New Title", 
         imageUrl:"",
    

      show: true,
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      const a =[this.textarea,this.title,this.imageUrl]
      this.$emit('data',a)
      
 
    },
  
    
  },
};
</script>