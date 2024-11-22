<script setup>
import { ref, onMounted } from 'vue'

// reactive state
const count = ref(0)

// function to increment count and log its value
function increment() {
  count.value++
  console.log(`Count increased to: ${count.value}`)
}

// lifecycle hook
onMounted(() => {
  console.log(`The initial count is ${count.value}.`)
})
</script>

<template>
  <div class="container">
    <h1>Button Counter!</h1>
    <button @click="increment" class="green-button">
      Count is: {{ count }}
    </button>
  </div>
</template>

<style>
/* Center content */
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh; /* Full screen height */
}

/* Style for the button */
.green-button {
  background-color: green;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 1.2rem;
  border-radius: 5px;
  cursor: pointer;
}

.green-button:hover {
  background-color: darkgreen;
}

/* Title styling (optional customization) */
h1 {
  margin-bottom: 20px;
  font-family: Arial, sans-serif;
  font-size: 2rem;
  color: #333;
}
</style>
