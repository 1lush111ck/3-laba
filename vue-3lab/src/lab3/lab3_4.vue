<script setup>
import { ref } from 'vue'

const selected = ref(null)
const directions = [
  'Кораблестроение и океанотехника',
  'Информатика и вычислительная техника',
  'Программная инженерия',
  'Электроэнергетика и электротехника',
  'Теплоэнергетика и теплотехника',
  'Строительство',
  'Машиностроение',
  'Управление качеством',
]
</script>

<template>
  <v-card>
    <v-card-title>4 Задание</v-card-title>
    <v-card-text>
      <v-autocomplete v-model="selected" :items="directions" label="Направление бакалавриата ИСМАРТ" />
      <div v-if="selected">Выбрано: {{ selected }}</div>
    </v-card-text>
  </v-card>
</template>
