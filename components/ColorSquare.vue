<template>
  <div class="container">
    <div class="square" :style="{ backgroundColor: `hsl(166, ${saturation}%, ${light}%)` }">
      <p class="center-text">{{ text }}</p>
    </div>
    <div class="controls">
      <label for="textInput">Text:</label>
      <input id="textInput" type="text" v-model="text" />

      <label for="saturationRange">Saturation:</label>
      <input id="saturationRange" type="range" v-model="saturation" min="0" max="100" />

      <label for="lightRange">Light:</label>
      <input id="lightRange" type="range" v-model="light" min="0" max="100" />


    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',
      saturation: 100,
      light: 50,
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.square {
  width: 500px;
  height: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
  color: white;
  font-size: 24px;
  font-weight: bold;
  text-align: center;
}

.center-text {
  margin: 0;
}

.controls {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.controls label {
  margin-top: 10px;
}

.controls input[type="range"] {
  width: 300px;
  margin-top: 5px;
}
</style>
