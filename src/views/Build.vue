<template>
  <div class="about">
    <h1>Create a bot</h1>
    <div class='flex-row'>
      <input type='text' placeholder='Name' v-model="name"/>
      <input type='text' placeholder='HP' v-model="hp"/>
      <input type='text' placeholder='ATK' v-model="atk"/>
    </div>
    <button @click='addBot(name,hp,atk)'>
      Submit
    </button>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        name:'',
        hp:null,
        atk:null
      }
    },
    props: {
      bots: Array
    },
    methods:{
      addBot(name, hitpoints, attack){
        hitpoints = parseInt(hitpoints,10);
        attack = parseInt(attack,10);
        this.bots.push({name, hitpoints, attack});
        this.clearState();
      },
      clearState(){
        this.name = '';
        this.hp = null;
        this.atk = null;
      }
    }
  }
</script>

<style>
.flex-row {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.flex-col {
  display: flex;
  flex-direction: column;
}
</style>