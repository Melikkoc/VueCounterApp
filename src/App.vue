<!--Composition API new way-->
<script setup>
import { ref } from 'vue';

const count = ref(0);

const addToCount = () => {
  count.value = count.value + 1;
};

const subtractFromCount = () => {
  count.value = count.value - 1;
};
</script>

<!--Options API old way
<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    addToCount() {
      this.count = this.count + 1;
    },
    subtractFromCount() {
      this.count = this.count - 1;
    },
  },
};
</script>
-->

<template>
  <main>
    <div>
      <h1>The current count is...</h1>
      <br />
      <h2>
        {{ count }}
      </h2>
      <button @click="subtractFromCount()">-</button>
      <button @click="addToCount()">+</button>
    </div>
  </main>
</template>
<!--scoped so that the css only applies for this file-->
<style scoped>
main {
  background-color: hsl(208, 100%, 93%);
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Arial, Helvetica, sans-serif;
}
h2 {
  font-size: 50px;
}
div {
  text-align: center;
  border: 2px solid black;
  background-color: rgb(190, 233, 248);
  border-radius: 15px;
}
button {
  padding: 2px 50px;
  margin: 30px;
  font-size: 4em;
  color: white;
  background-color: hsl(260, 57%, 64%);
  border: none;
  border-radius: 15px;
  cursor: pointer;
  transition: background-color 0.25s;
}
button:hover {
  background-color: hsl(260, 57%, 50%);
}
</style>
