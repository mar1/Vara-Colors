<template>
  <div class="container pt-12">
    <div class="square" :style="{ backgroundColor: `hsl(166, ${saturation}%, ${light}%)`, color: textColor }">
      <p class="center-text">{{ text }}</p>
    </div>
    <div class="controls">
      <label for="textInput">Text:</label>
      <input id="textInput" type="text" v-model="text" />

      <div class="color-options">
        <div class="color-square black" @click="setTextColor('black')"></div>
        <div class="color-square white" @click="setTextColor('white')"></div>
        <div class="color-square vara" @click="setTextColor('vara')"></div>
      </div>

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
      textColor: 'black',
    };
  },
  methods: {
    setTextColor(color) {
      if (color == "vara") {
        console.log("ok")
        this.textColor = "#00FFC4"
      }
      else {
        this.textColor = color;
      }
    }
  },
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 800px;
  margin: 0 auto;
  color: white;
}

.square {
  width: 300px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 20px;
  font-size: 24px;
  font-weight: bold;
  text-align: center;
  font-family: 'Nocember';
  letter-spacing: 2px;
  border: 3px solid hsl(166, 100%, 50%);
}

.controls {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.controls label {
  margin: 1rem;
  text-align: center;
  font-family: 'Nocember';
  padding: 0 0.5rem;
}

.controls input[type="text"] {
  color: black;
  text-align: center;
}

.controls input[type="range"] {
  width: 200px;
  margin-top: 5px;
  -webkit-appearance: none;
  appearance: none;
  background: hsl(166, 100%, 50%);
  height: 5px;
  outline: none;
  opacity: 0.7;
  transition: opacity 0.2s;
}

.controls input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 15px;
  height: 15px;
  border-radius: 4px;
  border: 1px solid hsl(166, 100%, 50%);
  background: hsl(166, 100%, 50%);
  cursor: pointer;
}

.controls input[type="range"]::-moz-range-thumb {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: hsl(166, 100%, 50%);
  cursor: pointer;
}

.color-options {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}

.color-square {
  width: 30px;
  height: 30px;
  margin-right: 10px;
  cursor: pointer;
  border: 1px solid #000;
}

.color-square.black {
  background-color: black;
  border: 1px solid white;
}

.color-square.white {
  background-color: white;
  border: 1px solid #000;
}

.color-square.vara {
  background-color: hsl(166, 100%, 50%);
  border: 1px solid hsl(166, 100%, 50%);
}
</style>
