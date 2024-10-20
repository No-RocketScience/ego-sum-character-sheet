<script setup>
import { ref } from 'vue'
const properties = defineProps({ name: String })

const input = ref(null)
</script>

<template>
    <div class="col">
        <div class="input-group mb-3">
            <span class="input-group-text" id="label-{{name.ToLowerCase()}}">{{ name }}</span>
            <input ref="input" id="{{name.ToLowerCase()}}" type="text" class="form-control"
                aria-describedby="name-text" />
        </div>
    </div>
</template>