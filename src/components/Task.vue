<template>
    <li
      :class="{
        taskIsWorking: !isDone,
        taskIsDone: isDone
      }"
      @click="toggleState">
      <span v-if="!isDone">👨‍🔧</span>
      <span v-else>🎯</span>
      {{ taskName }}
    </li>
</template>

<script>
export default {
  name: 'Task',
  props: ['taskName'],
  data () {
    return {
      isDone: false
    }
  },
  methods: {
    toggleState () {
      this.isDone = !this.isDone
    }
  }
}
</script>

<style scoped>
li {
  list-style: none;
  border: 3px solid blue;
  border-radius: 10px;
  width: 30vh;
  margin-bottom: 10px;
  padding: 5px;
  text-align: left;
  color: #ffffff;

}

li:hover {
  cursor: pointer;
}

.taskIsWorking {
  background-color: cyan;
}

.taskIsDone {
  background-color: #165284;
}
</style>
