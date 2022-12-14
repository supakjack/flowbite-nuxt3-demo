<script setup lang="ts">
const text = ref<string>('')
const list = ref<Array<string>>([])

function addToList(): void {
    list.value.push(text.value)
    alert("เพิ่มสำเร็จ")
}

function deleteAtIndex(index: number): void {
    list.value.splice(index, 1)
    alert("ลบสำเร็จ")
}

onMounted(() => {
    list.value = [
        'bek',
        'best'
    ]
})
</script>
<template>
    <!-- add form -->
    <AboutAddForm v-model="text" @click:add="addToList" />
    
    <!-- list -->
    <AboutList :list="list" @click:delete="deleteAtIndex" />
</template>
  