<template>
<div class="board">
  <Task taskName='Travailler sur mon projet perso' />
  <Task taskName='Faire le ménage' />
  <Task taskName='Jouer à Donjon de Naheulbeuk' />
  <Task taskName='Faire à manger' />
  <Task taskName='Jardiner' />

</div>
</template>

<script>
import Task from './components/Task.vue'

export default {
  name: 'Home',
  components: {
    Task
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
</style>
