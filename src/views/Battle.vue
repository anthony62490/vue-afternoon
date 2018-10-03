<template>
  <div class="home">
    <BotsList/>
  </div>
</template>

<script>
// @ is an alias to /src
import BotsList from '@/components/BotsList.vue'

export default {
  name: 'battle',
  components: {
    BotsList
  }
}
</script>

