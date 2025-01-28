<template>
  <v-container>
    <h1>Sub</h1>
    <p>This is the Sub Screen.</p>
    <v-btn color="secondary" @click="goHome">Go Back to Home</v-btn>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useRouter } from 'vue-router'

export default defineComponent({
  name: 'SubView',
  setup() {
    const router = useRouter()
    const goHome = () => {
      router.push({ name: 'Home' })
    }
    return {
      goHome,
    }
  },
})
</script>

<style scoped>
</style>
