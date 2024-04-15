<script setup lang="ts">

</script>

<template>
<header>
  <img alt="bla-bla" src="https://via.placeholder.com/50x50" />
  <span>cat energy</span>
  <button>
    <div></div>
    <div></div>
    <div></div>
  </button>
</header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 16px;
  font-size: 46px;
  button {
    display: flex;
    flex-direction: column;
    width: 50px;
    height: 30px;
    justify-content: space-between;
    background-color: transparent;
    border: none;
    div {
      height: 3px;
      width: 100%;
      background-color: black;
    }
  }
}
</style>
