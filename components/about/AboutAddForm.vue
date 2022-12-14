<script setup lang="ts">
defineProps<{
    modelValue: string
}>()

const emit = defineEmits<{
    (event: 'click:add'): void
    (event: 'update:modelValue', text: string): void
}>()
</script>

<template>
    <div>
        <input type="text" :value="modelValue" @input="(e) => {
            emit('update:modelValue', (e.target as HTMLTextAreaElement).value)
        }">
        <button @click="emit('click:add')">เพิ่ม</button>
    </div>
</template>