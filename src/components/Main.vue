<!-- script -->
<script setup>
import Noty from "noty";
import "noty/lib/noty.css";
import "noty/lib/themes/sunset.css";

const moveButtonRandom = () => {
  const buttons = document.querySelectorAll("#buttons #not");
  const random = Math.floor(Math.random() * buttons.length);
  console.log(random);
  console.log(buttons[random]);
  buttons[random].style.transform = `translate(${
    Math.random() * 100 - 50
  }px, ${Math.random() * 100 - 50}px)`;
};

const showNoty = () => {

  new Noty({
    text: "Esta bien seamos novios",
    // color dark, error, info, success, warning
    type: "success",
    timeout: 3000,
    progressBar: true,
    layout: "topRight",
    theme: "sunset",
    animation: {
      open: "noty_effects_open",
      close: "noty_effects_close",
    },
  }).show();

  console.log("Hola");
  console.log(new Noty());
};
</script>

<!-- template -->
<template>
  <h1>Quieres ser mi novia <span class="name">Dani</span> ?</h1>
  <div id="buttons">
    <button id="si" @click="showNoty">Si</button>
    <button
      id="not"
      @click="moveButtonRandom()"
      @mouseover="moveButtonRandom()"
    >
      No
    </button>
  </div>
</template>

<!-- Styles -->
<style scoped>
.name {
  color: #ffff80;
}
#buttons {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
button {
  margin: 0 10px;
  padding: 10px 20px;
  border-radius: 10px;
  border: none;
  background-color: #ffff80;
  color: #000;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
}
</style>
