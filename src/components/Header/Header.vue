<script setup>
import 'gridstack/dist/gridstack.min.css';
import { onMounted, ref } from 'vue'
import { GridStack } from 'gridstack';
import LabelText from '../LabelText/LabelText.vue';
import AdvancementPointsCounter from './AdvancementPointsCounter/AdvancementPointsCounter.vue';
import StatDisplay from './StatDisplay/StatDisplay.vue';

const nameInput = ref('Name')
const aspectInput = ref('Aspect')

const stats = ['STR', 'STA', 'AGI', 'DEX', 'CHA', 'WIL', 'ANI', 'SMA', 'DUR', 'RES', 'PER', 'ABI']

onMounted(() => { GridStack.init({ disableResize: true, itemClass: 'stat-display-container', margin: 0 }); });

</script>

<template>
    <div class="row">
        <LabelText :name="nameInput" />
        <AdvancementPointsCounter />
        <LabelText :name="aspectInput" />
        <div class="w-100" />
        <div class="col-12">
            <div class="row grid-stack">
                <StatDisplay v-for="stat in stats" :statName="stat" :id="stats.indexOf(stat)" />
            </div>
        </div>
    </div>
</template>