<script setup>
import DraggableListItem from '@/components/DraggableListItem.vue'

const props = defineProps({
  items: {
    type: Array,
    required: true
  }
})

import { ref, watch } from 'vue'

const dragItem = ref(null)
const dragOverItem = ref(null)
const dragOverIndex = ref(null)
const sortableItems = ref(props.items)

const handleDragStart = (e) => {
  dragItem.value = sortableItems.value.find((item) => item.id === e.target.dataset.itemId)
}

const handleDragOver = (e) => {
  e.preventDefault()
  dragOverItem.value = e.target.closest('li')
  dragOverIndex.value = sortableItems.value.findIndex((item) => item.id === dragOverItem.value.dataset.itemId)
  sortableItems.value.splice(dragOverIndex.value, 0, sortableItems.value.splice(sortableItems.value.indexOf(dragItem.value), 1)[0])
}

const handleDragEnd = () => {
  dragOverItem.value.classList.remove('opacity-50')
  dragItem.value = null
}

const handleDrop = (e) => {
  e.preventDefault()
}

// watch(
//   dragOverItem,
//   (newItem, oldItem) => {
//     if (newItem !== oldItem) {
//       newItem.classList.add('opacity-50')
//       if (oldItem) {
//         oldItem.classList.remove('opacity-50')
//       }
//     }
//   }
// )

</script>

<template>
  <ul class="flex flex-col gap-1">
    <DraggableListItem
      v-for="(item, index) in sortableItems"
      :key="index"
      :id="item.id"
      :draggingItemId="dragItem?.id"
      width="40rem"
      contentHeight="10rem"
      @dragstart="handleDragStart"
      @dragend="handleDragEnd"
      @dragover="handleDragOver"
      @drop="handleDrop"
    >
      <template #title>
        {{ item.header }}
      </template>
      <template #content>
        {{ item.content }}
      </template>
    </DraggableListItem>
  </ul>
</template>

<style scoped>

</style>