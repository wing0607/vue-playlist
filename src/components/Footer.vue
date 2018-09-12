<template>
    <footer>
      <h1>{{title1}}{{title}}</h1>
    </footer>
</template>

<script>
    export default {
        name: "app-footer",
      props:{
          title:{
            type:String
          }

      },
        data(){
          return{
            title1:"footer"
          }

      }
    }
</script>

<style scoped>
  footer{
    background: #222;
    padding: 10px;
  }
h1{ color: #000;
text-align: center}
</style>
