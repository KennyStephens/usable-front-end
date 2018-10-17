<template>
  <div>
    <h1 class="display-5 text-xs-center">Bitchin' Form Goes Here!</h1>
    <ul>
      <li v-for="(task, i) in taskItems" :key="i">{{ task.task }}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        taskItems: [
          {taskType: 'textArea', task: 'Task 1'},
          {taskType: 'textArea', task: 'Task 2'},
          {taskType: 'textArea', task: 'Task 3'},
        ]
      }
    }
  }
</script>
