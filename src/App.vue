<template>
  <UserCardComponent nickname="larik92" v-bind:adr="adr" v-bind:fullname="name" phone="82434234" v-bind:email="email"/>
  <button @click="getData()">Загрузить данные</button>
</template>

<script>
import UserCardComponent from './components/UserCardComponent.vue'

export default {
  name: 'App',
  components: {
    UserCardComponent
  },
  data(){
    return{
      email: 'larionov@gmail.com',
      name:"Виктор",
      adr: "Saint-Petersburg, Russia"
    }

  },
  methods:{
    getData(){
      this.axios.get('https://randomuser.me/api/')
       .then((response) => {
         this.email = response.data['results'][0]['email']
       })

    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
