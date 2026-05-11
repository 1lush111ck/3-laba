<script setup>
import { ref } from 'vue'

const num1 = ref(0)
const num2 = ref(0)
const result = ref(0)

const plush = () => result.value = Number(num1.value) + Number(num2.value)
const minus = () => result.value = Number(num1.value) - Number(num2.value)
const umnozh = () => result.value = Number(num1.value) * Number(num2.value)
const delenie = () => {
    const b = Number(num2.value)
    result.value = b !== 0 ? Number(num1.value) / b : 'Ошибка (деление на 0)'
}
const coren = () => {
    const a = Number(num1.value);
    const n = Number(num2.value);

    if (n === 0) {
        result.value = 'Ошибка (степень корня 0)';
        return;
    }

    if (a < 0 && n % 2 === 0) {
        result.value = 'Ошибка (отриц. под корнем)';
        return;
    }

    result.value = Math.pow(a, 1 / n);
}
const stepen = () => result.value = Math.pow(Number(num1.value), Number(num2.value))
const percent = () => result.value = (Number(num1.value) * Number(num2.value)) / 100
</script>

<template>
    <v-card>
        <v-card-title>2 Задание: Калькулятор</v-card-title>
        <v-card-text>
            <v-text-field v-model="num1" label="Число А (или основание)" type="number"></v-text-field>
            <v-text-field v-model="num2" label="Число Б (или степень/процент/степень корня)" type="number"></v-text-field>
            
            <div class="d-flex flex-wrap gap-2 mb-4" style="gap: 10px;">
                <v-btn @click="plush" color="blue">+</v-btn>
                <v-btn @click="minus" color="blue">-</v-btn>
                <v-btn @click="umnozh" color="blue">*</v-btn>
                <v-btn @click="delenie" color="blue">/</v-btn>
                <v-btn @click="coren" color="blue">√ (A)</v-btn>
                <v-btn @click="stepen" color="blue">A^B</v-btn>
                <v-btn @click="percent" color="blue">% от A</v-btn>
            </div>

            <v-divider></v-divider>
            <div>Результат: {{ result }}</div>
        </v-card-text>
    </v-card>
</template>