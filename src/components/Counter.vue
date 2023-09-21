<script setup>
import { ref } from "vue";

const value = ref(1);
</script>

<template>
  <div class="wrapper">
    <h1>Vuex Counter</h1>
    <h1 class="counter">{{ $store.state.counter }}</h1>
    <div class="btns">
      <button class="btn">-</button>
      <input v-model="value" class="input" type="number" />
      <button class="btn">+</button>
    </div>
  </div>
</template>

<style lang="scss">
.wrapper {
  text-align: center;
  .counter {
    font-size: 5rem;
  }
  .btns {
    display: flex;
    gap: 12px;
    align-items: center;
    .input {
      padding: 10px;
      border: none;
      outline: none;
      text-align: center;
    }
    .btn {
      display: inline-block;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      border: none;
    }
  }
}
</style>
