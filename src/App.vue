<template>
  <Places>
    <template #country="{id, place, log}">
      {{id}}{{place}}

      <button @click="log">Click</button>
    </template>

    <template #city="{id, place}">
      {{id}}{{place}}
    </template>
  </Places>
</template>

<script>
import Places from "./components/Places.vue";

export default {
  name: "App",
  components: {
    Places,
  },
};
</script>
