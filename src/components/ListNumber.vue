<template>
  <div class="list-container">
    <button @click="toggleList">Toggle List</button>
    <button @click="pushNumber">Push Number</button>
    <button @click="popNumber">Pop Number</button>
    <button @click="reverseList">Reverse List</button>

    <ul v-if="show && list.length" class="styled-list">
      <li v-for="item in list" :key="item" class="list-item">{{ item }}</li>
    </ul>
    <p v-else-if="list.length">List is not empty, but hidden.</p>
    <p v-else>List is empty.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true,
      list: [1, 2, 3]
    }
  },
  methods: {
    toggleList() {
      this.show = !this.show
    },
    pushNumber() {
      this.list.push(this.list.length + 1)
    },
    popNumber() {
      this.list.pop()
    },
    reverseList() {
      this.list.reverse()
    }
  }
}
</script>
   
<style scoped>
.list-container {
  max-width: 600px;
  margin: auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
  margin-top: 20px;
}

button {
  margin: 5px;
  padding: 10px 15px;
  background-color: #007bff;
  color: #ffffff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #0056b3;
}

.styled-list {
  list-style-type: none;
  padding: 0;
  margin-top: 20px;
}

.list-item {
  padding: 10px;
  margin: 5px 0;
  background-color: #ffffff;
  border: 1px solid #ddd;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.list-item:hover {
  background-color: #f1f1f1;
}
</style>