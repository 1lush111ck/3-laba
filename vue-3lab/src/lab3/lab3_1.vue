<script setup>
import { ref } from 'vue'

const text = ref('')
</script>

<template>
    <v-card>
        <v-card-title>1 Задание</v-card-title>
        <v-card-text>
            <v-text-field v-model="text"></v-text-field>
            <div>Ваш текст: {{ text }}</div>
        </v-card-text>
    </v-card>
</template>
