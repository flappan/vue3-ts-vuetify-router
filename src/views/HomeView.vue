<template>
  <v-container>
    <h1>Home 画面</h1>
    <p>ここはホームです</p>
    <v-btn color="primary" @click="goToSub">Sub 画面へ</v-btn>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useRouter } from 'vue-router'

export default defineComponent({
  name: 'HomeView',
  setup() {
    const router = useRouter()
    const goToSub = () => {
      router.push({ name: 'Sub' })
    }
    return {
      goToSub,
    }
  },
})
</script>

<style scoped>
</style>
