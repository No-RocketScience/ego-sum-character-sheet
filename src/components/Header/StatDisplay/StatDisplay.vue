<script setup>
import { ref } from 'vue';

const props = defineProps({ statName: String, id: Number });

const number = ref(null);

</script>
<template>
    <div class="stat-display-container">
        <span class="stat-info stat-name">{{ statName || 'StatName' }}</span>
        <span class="stat-info stat-number" ref="number">1</span>
    </div>
</template>

<style lang="css" scoped>
.stat-display-container {
    --width: 80px;
    width: var(--width);
    height: calc(var(--width) + (var(--width) * (5/16)));
    margin: .25em;
}

.stat-info {
    border: 3px solid #1a1a1a;
    flex: 0 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
}

.stat-name {
    border-radius: 5px;
    padding: 0 .25em;
    background-color: white;
    font-size: 25px;
    --width-reduction: 20px;
    width: calc(var(--width) - var(--width-reduction));
    margin-left: calc(var(--width-reduction) / 2);
    margin-right: calc(var(--width-reduction) / 2);
}

.stat-number {
    font-size: calc(var(--width) / 2);
    font-weight: bold;
    border-radius: 100%;
    padding: .75em;
    position: relative;
    top: calc(var(--width) * (-5/16));
    z-index: -1;
    height: var(--width);
    width: var(--width);
}
</style>