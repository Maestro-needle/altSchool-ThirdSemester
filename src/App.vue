<template>
  <div>
    <center>
      <h1>Hello</h1>
      <h2>My name is Yusuf Mariam</h2>
      <h2>This is my Third semester Altschool</h2>
      <h1 :class="counter">Counter: {{ counter }}</h1>
      <button :class="increment" @click="increment">Increment</button>
      <button :class="decrement" @click="decrement">Decrement</button>
      <button :class="reset" @click="reset">Reset</button>
    </center>
  </div>
</template>

<script>
export default {
  computed: {
    counter() {
      return this.$store.getters.counter;
    },
  },
  methods: {
    increment() {
      this.$store.dispatch("increment");
    },
    decrement() {
      this.$store.dispatch("decrement");
    },
    reset() {
      this.$store.dispatch("reset");
    },
  },
};
</script>

<style>
body {
  margin: 0;
  background: #5592dc;
  display: flex;
  height: 100vh;
  width: 100vw;
  justify-content: center;
  place-items: center;
}
.increment {
  padding-left: 5px;
}
</style>
