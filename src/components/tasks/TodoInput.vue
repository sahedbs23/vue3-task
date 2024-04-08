<template>
  <div>
    <input
      v-model="newTodo"
      class="mr-2 rounded border border-gray-400 p-2"
      type="text"
      @keyup.enter="addTodo"
    >
    <button
      class="rounded bg-blue-500 py-2 px-4 font-bold text-white hover:bg-blue-700"
      @click="addTodo"
    >
      Add Todo
    </button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  emits: ['add-todo'],
  setup(props, { emit }) {
    const newTodo = ref('');

    const addTodo = () => {
      if (newTodo.value.trim() !== '') {
        emit('add-todo', newTodo.value);
        newTodo.value = '';
      }
    };

    return {
      newTodo,
      addTodo,
    };
  },
};
</script>
