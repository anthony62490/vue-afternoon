<template>
  <div>
    <div class='list'>
      <div class='card' :key='i' v-for="(e, i) in bots">
        <Bot :name='e.name' :hp='e.hitpoints' :atk='e.attack' :pick='pickBot' :index='i'/>
      </div>
    </div>
    {{bot1}}
    {{bot2}}
  </div>
</template>

<script>
  import Bot from '@/components/Bot.vue';
  export default {
    components:{
      Bot: Bot
    },
    props:{
      bots: Array,
      bot1: Number || null,
      bot2: Number || null
    },
    methods:{
      pickBot(i){
        if(!this.bot1){
          this.bot1 = i;
        }
        else if(!this.bot2){
          this.bot2 = i;
          this.pickWinner(this.bot1,this.bot2);
        }
        console.log('bots', this.bot1, this.bot2);
      },
      pickWinner(one, two){
        if(Math.random() > 0.5){
          alert(`${this.bots[one].name} wins!`);
        }
        else {
          alert(`${this.bots[two].name} wins!`);
        }
        this.bot1 = null;
        this.bot2 = null;
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