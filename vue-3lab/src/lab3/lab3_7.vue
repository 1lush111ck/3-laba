<script setup>
import { ref } from 'vue'

const selected = ref([])
</script>

<template>
  <v-card>
    <v-card-title>Задание 7</v-card-title>
    <v-card-text>
      <v-checkbox v-model="selected" label="Опция 1" value="Опция 1" />
      <v-checkbox v-model="selected" label="Опция 2" value="Опция 2" />
      <v-checkbox v-model="selected" label="Опция 3" value="Опция 3" />
      <div>Выбрано: {{ selected.join(', ') }}</div>
    </v-card-text>
  </v-card>
</template>