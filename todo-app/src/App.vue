<script>
export default {
  data() {
    return {
      todos: [
        {
          id: 1,
          text: "Learn JavaScript",
          completed: false
        },
        {
          id: 2,
          text: "Build a to-do list app",
          completed: false
        },
        {
          id: 3,
          text: "Master React",
          completed: true
        }
      ]
    }
  }
}
</script>

<template>
  <header>

    <div class="">
      <h1>TODO App</h1>
    </div>
  </header>

  <main>
    <div v-for="(task, index) in todos" className="todoInfo" :key="task.id">
      <span className="todoTitle">
        {{ task.text }}
      </span>
      <button className="button">Edit</button>
      <button className="buttonDelete">Delete</button>
    </div>
  </main>
</template>

<style scoped></style>
