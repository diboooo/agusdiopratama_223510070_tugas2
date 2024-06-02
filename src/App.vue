<template>
  <div id="app">
    <h1>Hello, Saya Agusdio Pratama</h1>
    <p>Ini adalah tugas 2 PBK </p>

    <!-- Input Text Element -->
    <input type="text" v-model="inputText" placeholder="Type something...">

    <!-- Combined Class and Style Bindings -->
    <div :class="{ highlight: isHighlighted, 'text-bold': isBold }" 
         :style="{ fontSize: fontSize + 'px', color: textColor }">
      {{ message }}
    </div>

    <!-- Buttons to Trigger Event Listeners -->
    <button @click="toggleHighlight">ada background nya loh</button>
    <button @click="toggleBold">di tekan jadi tebal</button>
    <button @click="increaseFontSize">jangan di pencet nanti gede</button>
    <button @click="changeTextColor">bisa ubah warna nih</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      message: 'DIO GANTENG',
      isHighlighted: false,
      isBold: false,
      fontSize: 16,
      textColor: 'black'
    }
  },
  methods: {
    toggleHighlight() {
      this.isHighlighted = !this.isHighlighted;
    },
    toggleBold() {
      this.isBold = !this.isBold;
    },
    increaseFontSize() {
      this.fontSize += 1;
    },
    changeTextColor() {
      this.textColor = this.textColor === 'black' ? 'blue' : 'pink';
    }
  }
}
</script>

<style>
.highlight {
  background-color: yellow;
}
.text-bold {
  font-weight: bold;
}
</style>
