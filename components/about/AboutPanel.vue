<script setup lang="ts">
defineProps<{
    count: number
}>()
</script>

<template>
    <section>
        count : {{ count }}
        <p>This page will be displayed at the /about route.</p>
    </section>
</template>