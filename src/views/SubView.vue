<template>
  <v-container>
    <h1>Sub 画面</h1>
    <p>Sub 画面です。</p>
    <v-btn color="secondary" @click="goHome">Home へ戻る</v-btn>
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
