<template>
  <div class="container">
    <div id="panel1" class="panel active">
      <h3>Explore the world</h3>
    </div>
    <div id="panel2" class="panel">
      <h3>Wild Forest</h3>
    </div>
    <div id="panel3" class="panel">
      <h3>Sunny Beach</h3>
    </div>
    <div id="panel4" class="panel">
      <h3>City on Winter</h3>
    </div>
    <div id="panel5" class="panel">
      <h3>Mountain - Clouds</h3>
    </div>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'

onMounted(() => {
  const panels = document.querySelectorAll('.panel')

  panels.forEach((panel) => {
    panel.addEventListener('click', () => {
      removeActiveClasses()
      panel.classList.add('active')
    })
  })

  function removeActiveClasses() {
    panels.forEach((panel) => {
      panel.classList.remove('active')
    })
  }
})
</script>

<style scoped>
#panel1 {
  background-image: url('https://images.unsplash.com/photo-1682687981922-7b55dbb30892?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80');
}

#panel2 {
  background-image: url('https://images.unsplash.com/photo-1516571137133-1be29e37143a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1174&q=80');
}

#panel3 {
  background-image: url('https://images.unsplash.com/photo-1579493933703-70473cdf84f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80');
}

#panel4 {
  background-image: url('https://images.unsplash.com/photo-1613069344419-ce7e1e869daa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80');
}

#panel5 {
  background-image: url('https://images.unsplash.com/photo-1563293756-857fc846d0d1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1185&q=80');
}

.container {
  height: 100%;
  display: flex;
  align-items: center;
  width: 90vw;
}

.panel {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 70vh;
  border-radius: 50px;
  cursor: pointer;
  flex: 0.5;
  margin: 10px;
  position: relative;
  transition: flex 0.7s ease-in;
}
.panel h3 {
  color: #fff;
  font-size: 1.5rem;
  position: absolute;
  bottom: 1.25rem;
  left: 1.25rem;
  margin: 0;
  opacity: 0;
}

.panel.active {
  flex: 5;
}

.panel.active h3 {
  opacity: 1;
  transition: opacity 0.3s ease-in 0.4s;
}

@media (max-width: 30rem) {
  .container {
    width: 100vw;
  }

  .panel:nth-of-type(4),
  .panel:nth-of-type(5) {
    display: none;
  }
}

@media (max-width: 25rem) {
  .container {
    width: 100vw;
  }

  .panel:nth-of-type(3),
  .panel:nth-of-type(4),
  .panel:nth-of-type(5) {
    display: none;
  }
}
</style>
