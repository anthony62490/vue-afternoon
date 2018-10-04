<template>
  <div class="home">
    <!-- Don't forget to bind props or the name will be treated as a string -->
    <BotsList :bots='bots'/>
  </div>
</template>

<script>
// @ is an alias to /src
import BotsList from '@/components/BotsList.vue'

export default {
  name: 'battle',
  props:{
    bots: Array
  },
  components: {
    BotsList
  }
}
</script>

