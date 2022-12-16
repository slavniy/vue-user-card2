<template>
  <UserCardComponent nickname="larik92" adr="SPb, Russia" fullname="Larionov Viktor Igorevich" phone="82434234" email="larionov@mail.ru"/>
</template>

<script>
import UserCardComponent from './components/UserCardComponent.vue'

export default {
  name: 'App',
  components: {
    UserCardComponent
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
