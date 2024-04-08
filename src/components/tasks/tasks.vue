<template>
  <div
    class="grid grid-cols-3 gap-4"
  >
    <div
      class="col-span-1 p-4"
    >
      <todo-list :todos="todos" />
    </div>
    <div
      class="col-span-2 p-4"
    >
      <todo-input @add-todo="addTodo" />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import TodoInput from '@/components/tasks/TodoInput.vue';
import TodoList from '@/components/tasks/TodoList.vue';

export default {
  components: {
    TodoInput,
    TodoList,
  },
  setup() {
    const todos = ref([]);

    const addTodo = (todo) => {
      todos.value.push(todo);
    };

    return {
      todos,
      addTodo,
    };
  },
};
</script>
