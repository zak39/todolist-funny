<template>
<div class="board">
  <Task
    v-for="task in tasks"
    :key="task.name"
    :taskName="task.name" />
  <input
    type="text"
    class="createTask"
    @keyup.enter="createTask"
    v-model=taskName
    placeholder="🌷 Jardiner" />
</div>
</template>

<script>
import Task from './components/Task.vue'

export default {
  name: 'Home',
  components: {
    Task
  },
  data () {
    return {
      taskName: '',
      tasks: [
        {
          name: 'Travailler sur mon projet perso'
        },
        {
          name: 'Faire le ménage'
        },
        {
          name: 'Jouer à Donjon de Naheulbeuk'
        },
        {
          name: 'Faire à manger'
        },
        {
          name: 'Jardiner'
        }
      ]
    }
  },
  methods: {
    createTask () {
      this.tasks.push({ name: this.taskName })
      this.taskName = ''
    }
  }
}
</script>

<style>
.board {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

.createTask {
  border: 1px solid transparent;
  border-bottom: 1px solid #154c79;
  margin-top: 30px;
  padding: 8px;
  text-align: left;
}

.createTask:focus{
  font-size: 15px;
}

</style>
