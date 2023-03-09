<script setup>
import { ref } from 'vue'
import MyButton from '@/components/MyButton.vue'

const loading = ref(false)

const load = () => {
  loading.value = true
  setTimeout(() => (loading.value = false), 1000)
}

const appendText = ref('dodatkowa treść')
</script>

<template>
  <my-button 
      :loading="loading"
      :disabled="loading"
      color="primary"
      size="small"
      class="button"
      @click="load"
  >
    <template #prepend>
      <v-icon icon="mdi-checkbox-marked-circle" />
    </template>

    Przycisk

    <template #append>
      {{ appendText }}
    </template>

    <template #loader>
      <v-icon light>mdi-cached</v-icon>
    </template>
  </my-button>
</template>
