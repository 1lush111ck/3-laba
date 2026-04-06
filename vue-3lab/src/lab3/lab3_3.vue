<script setup>
import { ref, computed } from 'vue'
const date = ref(null)
</script>

<template>
    <v-card>
        <v-card-title>3 задание</v-card-title>
        <v-card-text>
            <v-date-picker v-model="date" />
            <v-text-field :model-value="date ? date.toLocaleDateString() : ''" label="Выбранная дата" readonly />
        </v-card-text>
    </v-card>
</template>