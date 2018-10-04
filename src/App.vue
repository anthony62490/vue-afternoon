<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Roster</router-link> |
      <router-link to="/build">Build</router-link>
    </div>
    <router-view :bots='bots'/>
  </div>
</template>

<script>
  import Bot from '@/components/Bot.vue';
  import BotsList from '@/components/BotsList.vue';
  export default {
    components:{
      Bot,
      BotsList
    },
    data() {
      return {
        bots:[
          {name:'Nightsass', hitpoints:50, attack:4},
          {name:'Crusher', hitpoints:20, attack:8},
          {name:'B0nb0n', hitpoints:40, attack:3},
          {name:'Breakdown', hitpoints:60, attack:2},
          {name:'Dodger', hitpoints:5, attack:20}
        ],
        bot1:null,
        bot2:null
      }
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  border: 2px solid black;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
