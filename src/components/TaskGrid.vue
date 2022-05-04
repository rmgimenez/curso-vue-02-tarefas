<template>
  <div class="task-grid">
      <template>
          <Task v-for="task in tasks" :key="task.name" :task="task">{{ task.name }}</Task>
      </template>
  </div>
</template>

<script>
import Task from './Task.vue';

export default {
  components: { Task },
  props: {
    tasks: { type: Array, required: true }
  }
};
</script>
  
<style>
  .task {
    box-sizing: border-box;
    width: 350px;
    height: 150px;
    padding: 10px;
    border-radius: 8px;
    font-size: 2rem;
    font-weight: 300;
    cursor: pointer;
    user-select: none;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .pending {
    border-left: 12px solid #b73229;
    background-color: #f44336;
  }

  .done {
    color: #ddd;
    border-left: 12px solid #0a8f08;
    background-color: #4caf50;
    text-decoration: line-through;
  }
</style>
