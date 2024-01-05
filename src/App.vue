<script> 
export default {
  data(){
    return {
        input_title : "",
        input_text : "Default Text",
      posts : [
        {
          id: 1,
          title : "First title",
          body : "First body"
        }, 
        {
          id : 2,
          title : "Second title",
          body : "Second body"
        }
      ] 
    }
  }, 
  methods : {
    clickSubmit(){
        this.input_title = "RESETTED TITLE"
        this.input_text  = 'RESETTED TEXT'
        
    }
  }
}
</script>

<template>
  <div class="post" v-for="post in posts">
    <div>{{ post.title }}</div>
    <div>{{ post.body }}</div>
  </div>
  <form action="" @submit.prevent="clickSubmit">
    <input  type="text" v-model="input_title">
    <input type="text" v-model="input_text">
    <button type="submit">23w4</button>
</form>
    
</template>

<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
</style>