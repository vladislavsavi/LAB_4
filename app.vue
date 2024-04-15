<template>
  <div>
   Hello
    {{count}}
    <button @click="count ++">click</button>
  </div>
</template>

<script lang="ts" setup>
const count = useState(() => 0);
</script>
