<template>
    <div>
        <input v-model="userInput" placeholder="Nhập giá trị tại đây"/>
        <p>Giá trị bạn nhập là: {{ userInput }}</p>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const userInput = ref('FPL');
</script>