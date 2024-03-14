<script setup>
import ListContainer from './components/ListContainer.vue';

const items = [
  {
    id: '1',
    header: 'Frontend',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '2',
    header: 'Learning Vue 4',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '3',
    header: 'Learning Vue 5',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '4',
    header: 'Learning Vue 7',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '5',
    header: 'Learning Vue 10',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '6',
    header: 'Learning Vue 47',
    content: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi accusamus unde atque exercitationem maiores sunt pariatur dicta ipsum eos aspernatur quam veniam, porro iure cum repellendus voluptatibus non! Similique, culpa.'
  },
  {
    id: '7',
    header: 'Learning Vue 89',
    content: 'yutmuttyetrby 7777'
  },
  {
    id: '8',
    header: 'Learning Vue 320',
    content: 'fr56u7io8l9k7ij6h 8888'
  }
]
</script>

<template>
  <main>
    <ListContainer :items="items" />
  </main>
</template>

<style scoped>

</style>