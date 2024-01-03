<script>
export default {
  data() {
    return {
      number: 0,
      max: 10,
      min: 5
    }
  },

  methods: {
    increment() {
      if(this.number < this.max) {
        this.number++
      }
    },
    decrement() {
      if(this.number > 0) {
        this.number--
      } else {
        alert('Number is already 0');
      }
    },
    reset() {
      this.number = 0;
    }
  }
}
</script>

<template>
  <div style="display: flex; justify-content: center;">
    <div style="display: flex; flex-direction: column; align-items: center">
      <h1 style="color: white; font-size: 36px; font-weight: bold">COUNTER</h1>
      <h1 style="margin: 30px 0; color: white; font-size: 36px; font-weight: bold">{{ number }} </h1>
      <div style="display: flex; gap: 15px; margin-top: 20px">
        <button type="button" @click="decrement">Decrement</button>
        <button type="button" @click="reset">Reset</button>
        <button type="button" @click="increment">Increment</button>
      </div>
    </div>
  </div>
</template>

<style scoped>

button {
  border: none;
  padding: 8px 20px;
  border-radius: 50px;
}

button:first-child {
  background-color: yellow;
}

button:nth-child(2) {
  background-color: red;
}

button:last-child {
  background-color: green;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
