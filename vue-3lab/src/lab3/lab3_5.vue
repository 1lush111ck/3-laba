<script setup>
import { ref } from 'vue'

const dialog = ref(false)
const field1 = ref('')
const field2 = ref('')

function onSubmit() {
  console.log('Поле 1:', field1.value)
  console.log('Поле 2:', field2.value)
}
</script>

<template>
  <v-card>
    <v-card-title>Задание 5</v-card-title>
    <v-card-text>
      <v-btn @click="dialog = true">Открыть диалог</v-btn>
      <v-dialog v-model="dialog" max-width="400">
        <v-card>
          <v-card-title>Диалог</v-card-title>
          <v-card-text>
            <v-text-field v-model="field1" label="Поле 1" />
            <v-text-field v-model="field2" label="Поле 2" />
          </v-card-text>
          <v-card-actions>
            <v-btn @click="onSubmit">Вывести в консоль</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-card-text>
  </v-card>
</template>