<template>
  <div class="wrapper">
    <h2>BULMA Todo List</h2>
    <div class="todolist__container">
      <input
        class="input is-primary todolist__input"
        type="text"
        placeholder="todoを入力してください。"
        v-model="this.newItem"
      />
      <button class="button is-primary todolist__button" v-on:click="addTodo()">
        ADD
      </button>
    </div>

    <div class="todolist__items">
      <ul>
        <TodoListItem
          v-for="(item, index) in todolist"
          v-bind:key="index"
          v-bind:item="item"
        />
      </ul>
    </div>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem";

export default {
  components: {
    TodoListItem,
  },
  data: function() {
    return {
      newItem: "",
      todolist: [],
    };
  },
  methods: {
    addTodo: function() {
      if (this.newItem === "") return;
      this.todolist.push(this.newItem);
      this.newItem = "";
    },
  },
};
</script>

<style scoped>
.wrapper {
  margin: 0 auto;
  margin-top: 80px;
  max-width: 660px;
  width: 100%;
  text-align: center;
}
.todolist__container {
  margin: 30px 20px 0px;
  display: flex;
}
.todolist__input {
  flex-grow: 1;
}
.todolist__button {
  margin-left: 30px;
}
.todolist__items {
  margin: 30px;
  text-align: start;
}
</style>
