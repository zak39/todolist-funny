<template>
    <li
      :class="{
        taskIsWorking: !isDone,
        taskIsDone: isDone
      }"
      @click="toggleState">
      <span v-if="!isDone">👨‍🔧</span>
      <span v-else>❌</span>
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
  border: 1px solid #2596be;
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
  background-color: #51abcb;
  transition: 0.2s;
}

.taskIsDone {
  background-color: #165284;
  border: 1px solid transparent;
  transition: 0.2s;
}
</style>
