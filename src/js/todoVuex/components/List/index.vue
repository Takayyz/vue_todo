<template lang="html">
  <ul class="todos__list">
    <app-list-item
      v-for="todo in todos"
      :todo="todo"
      :key="todo.id"
    />
  </ul>
</template>

<script>
import ListItem from '../ListItem';

export default {
  components: {
    appListItem: ListItem,
  },
  props: {
    todos: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
