<template>
  <div class='list'>
    <div class='card' :key='i' v-for="(e, i) in getBots">
      <Bot :name='e.name' :hp='e.hitpoints' :atk='e.attack'/>
    </div>
  </div>
</template>

<script>
  import Bot from '@/components/Bot.vue';
  export default {
    components:{
      Bot: Bot
    },
    data() {
      return {
        begin: 'begin.',
        bots:[
          {name:'Nightsass', hitpoints:50, attack:4},
          {name:'Crusher', hitpoints:20, attack:8},
          {name:'B0nb0n', hitpoints:40, attack:3},
          {name:'Breakdown', hitpoints:60, attack:2},
          {name:'Dodger', hitpoints:5, attack:20}
        ]
      }
    },
    // methods:{
    //   addBot
    // }
    computed:{
      getBots(){
        return this.bots.slice();
      }
    }
  }
</script>

<style>
.list {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
.card {
  border: 1px solid blue;
  width: 250px;
}
</style>