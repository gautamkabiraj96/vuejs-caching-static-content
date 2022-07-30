<template>
  <div id="app">
    <div v-once>Hello there!</div>
    <p v-once>
      Please click the Increase button to increase counter value and Decrease
      button to decrease counter value.
    </p>
    <div>
      <h3>Counter: {{ counter }}</h3>
      <button @click="increaseCounter">Increase</button>
      <button @click="decreaseCounter">Decrease</button>
    </div>
    <div v-once class="np-credits">wwww.nightprogrammer.com</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increaseCounter() {
      this.counter++;
    },
    decreaseCounter() {
      this.counter--;
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 24px;
}

p {
  max-width: 400px;
}

button {
  background-color: #004cbe;
  color: #ffffff;
  border: 0px;
  border-radius: 6px;
  padding: 6px 20px;
  margin-right: 1em;
  cursor: pointer;
  transition: all 0.3s;
}

button:hover {
  background-color: #2f79e7;
  transition: all 0.3s;
}

.np-credits {
  font-size: 12px;
  margin-top: 12px;
  color: #4b4b4b;
}
</style>