<template>
  <div class="box todolist__item">
    {{ item }}
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.todolist__item {
  margin-bottom: 1rem;
}
</style>
