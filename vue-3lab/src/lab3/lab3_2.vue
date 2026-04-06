<script setup>
import { ref, computed } from 'vue'

const base = ref(0)
const exp = ref(0)
const result = computed(() => Math.pow(Number(base.value), Number(exp.value)))
</script>

<template>
    <v-card>
        <v-card-title>2 задание</v-card-title>
        <v-card-text>
            <v-text-field v-model="base" label="Основание" type="number"></v-text-field>
            <v-text-field v-model="exp" label="Степень" type="number"></v-text-field>
            <div>Результат: {{ result }}</div>
        </v-card-text>
    </v-card>
</template>