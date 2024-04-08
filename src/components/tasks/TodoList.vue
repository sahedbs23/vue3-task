<template>
  <div>
    <ul>
      <li
        v-for="(todo, index) in todos"
        :key="index"
        class="mb-2 flex items-center justify-between rounded border border-gray-400 p-2"
      >
        <span>
          <i class="far fa-square mr-2"></i> {{ todo }}
        </span>
        <img
          src="https://daisyui.com/images/stock/photo-1534528741775-53994a69daeb.jpg"
          alt="Profile Picture"
          class="h-8 w-8 rounded-full"
        >
      </li>
    </ul>
  </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css';

export default {
  props: {
    todos: {
      type: Array,
      required: true,
    },
  },
};
</script>
