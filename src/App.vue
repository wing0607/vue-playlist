<template>
  <div id="app">
    <app-header v-on:titleChanged="updateTitle($event)" v-bind:title="title"></app-header>
    <h1>{{title}}</h1>
    <users v-bind:users="users"></users>
    <users v-bind:users="users"></users>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
//局部注册组件
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'
export default {
  name: 'App',
  data(){
    return{
      users: [{name:"Henery",job:"web前端",show:false},
        {name:"Bucky",job:"web前端",show:false},
        {name:"Emily",job:"web前端",show:false},],
      title:"app"
    }
  },
  methods:{
    updateTitle(title){
      this.title=title
    }
  },
  components: {

    "users":Users,
    "app-header":Header,
    "app-footer":Footer

  }
}
</script>

<style>
  body{ padding: 0; margin: 0;}
h1{ color: peachpuff}
</style>
