

<template>

  <div>
      <HelloWorld
        :items= "items"
      />
  </div>

</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { ref } from "vue";
import type User from "../src/types/User";

const items = ref<User[]>([
    {
      name: "Jean",
      age: 23
    },
    {
      name: "Lucie",
      age: 25
    },
  ])
</script>