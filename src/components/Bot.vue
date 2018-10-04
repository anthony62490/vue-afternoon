<template>
  <div>
    <p>Name: <strong>{{name}}</strong></p>
    <p>Max HP: <strong>{{hp}}</strong></p>
    <p>Attack Power: <strong>{{atk}}</strong></p>
    <button @click='pick(index)'>Fight!</button>
    <button>Delete</button>
  </div>
</template>

<script>
  export default {
    props: {
      name: {
        type: String,
        required: true,
        default: 'NO NAME'
      },
      hp: {
        type: Number,
        required: true
      },
      atk: {
        type: Number,
        required: true
      },
      pick: {
        type: Function,
        required: true
      },
      index: {
        type: Number,
        required: true
      }
    }
  }
</script>

<style>
</style>