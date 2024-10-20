<script setup>
import AdvancementPointsCounter from './Counters/AdvancementPointsCounter.vue';
import SpentCounter from './Counters/SpentCounter.vue';
</script>

<template>
    <div class="col">
        <div class="input-group mb-3">
            <AdvancementPointsCounter />
            <SpentCounter />
        </div>
    </div>
</template>