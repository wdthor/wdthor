<template>
  <button>
    <slot></slot>
  </button>
</template>

<style scoped>
button {
  border: none;
  font-size: 1.2rem;
  cursor: pointer;
  transition: text-shadow 0.3s, text-decoration-color 0.3s;
  padding: 2px;
  border-radius: 3px;
  text-decoration: underline;
  text-underline-position: auto;
  text-decoration-color: transparent;
}

button:hover {
  text-shadow: -0.5px 0 1px #99f;
  text-decoration-color: #99f;
}
</style>
