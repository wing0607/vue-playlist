<template>
  <div class="users">
    <ul>
      <li v-for="user in users">
        <p v-on:click="user.show=!user.show">{{user.name}}</p>
        <p v-show="user.show">{{user.job}}</p>
      </li>
    </ul>
<button v-on:click="deleteUser">删除</button>
  </div>

</template>

<script>
    export default {
        name: "users",
        //props:["users"],
        props:{
            users:{
              type:Array,
              required:true
            }
        },
        data(){
          return {

          }
        },
      methods:{
          deleteUser:function () {
            this.users.pop();
          }
      }
    }
</script>

<style scoped>

</style>
