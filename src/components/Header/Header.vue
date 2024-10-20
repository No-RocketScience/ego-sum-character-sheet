<script setup>
import { ref } from 'vue'
import LabelText from '../LabelText/LabelText.vue';
import AdvancementPointsCounter from '../AdvancementPointsCounter/AdvancementPointsCounter.vue';

const nameInput = ref('Name')
const aspectInput = ref('Aspect')
</script>

<template>
    <div class="row">
        <LabelText :name="nameInput" />
        <AdvancementPointsCounter />
        <LabelText :name="aspectInput" />
    </div>
</template>