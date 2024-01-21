<template>
  <div id="app">
    <div class="content">
      <h1>Joyeuse Anniversaire & Saint-Valentin, la Cat !</h1>
      <button @click="genererNumero">Quel sera le cadeau ?</button>
      <p v-if="numeroCadeau">Numéro du cadeau : {{ numeroCadeau }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      numeroCadeau: null
    };
  },
  methods: {
    genererNumero() {
      this.numeroCadeau = Math.floor(Math.random() * 15) + 1;
    }
  }
}
</script>

<style>
#app {
  background-image: url('./assets/portoRomantique.png');
  background-size: cover;
  background-position: center;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.content {
  text-align: center;
  background-color: rgba(255, 255, 255, 0.5);
  padding: 50px;
  margin: 50px;
  border-radius: 10px;
  backdrop-filter: blur(5px);
}

h1, button, p {
  color: white;
  backdrop-filter: blur(5px);
}

button {
  background-color: #cc0000;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  transition: transform 0.2s, background-color 0.2s;
}

button:hover {
  transform: scale(1.1);
  background-color: #990000;
}
</style>
