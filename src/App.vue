<template>
  <div>
    <h1 class="title">NANDA ALFIRANDA</h1>
    <p class="description">Ini adalah sebuah paragraf dengan</p>
    <input
      type="text"
      v-model="inputText"
      placeholder="Ketik sesuatu..."
      @keyup.enter="changeFontSize"
      class="input-field"
    />
    <p>Anda mengetik: {{ inputText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHighlighted: false,
      inputText: "",
      fontSize: 16,
    };
  },
  methods: {
    changeFontSize() {
      this.fontSize += 2;
    },
  },
};
</script>

<style scoped>
.title {
  font-size: 2rem;
  color: #fefefe;
  text-align: center;
}

.description {
  font-size: 1.2rem;
  color: #666;
  text-align: center;
}

.input-field {
  width: 100%;
  padding: 10px;
  font-size: 1rem;
  border: 2px solid #ccc;
  border-radius: 5px;
  margin-top: 10px;
}

.input-field:focus {
  border-color: #007bff;
  outline: none;
}
</style>
