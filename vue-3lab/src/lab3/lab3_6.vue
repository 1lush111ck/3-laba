<script setup>
import { ref } from 'vue'

const selected = ref(null)
</script>

<template>
  <v-card>
    <v-card-title>Задание 6</v-card-title>
    <v-card-text>
      <v-radio-group v-model="selected">
        <v-radio label="Вариант A" value="A" />
        <v-radio label="Вариант B" value="B" />
        <v-radio label="Вариант C" value="C" />
      </v-radio-group>
      <div>Выбрано: {{ selected }}</div>
    </v-card-text>
  </v-card>
</template>