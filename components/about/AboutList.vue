<script setup lang="ts">
defineProps<{
    list: Array<string>
}>()

const emit = defineEmits<{
    (event: 'click:delete', index: number): void
}>()
</script>

<template>
    <ul
        class="w-48 text-sm font-medium text-gray-900 bg-white rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600 dark:text-white">
        <div v-for="(text, index) in list">
            <li class="py-2 px-4 w-full rounded-t-lg border-b border-gray-200 dark:border-gray-600">
                {{ index }} : {{ text }}
                <button type="button"
                    class="focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900">Red</button>
            </li>
        </div>
    </ul>
</template>