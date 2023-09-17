

<template>
  <div>
    <h1
      v-text="title"
    ></h1>

    <h2
      v-text="subtitle"
    ></h2>

    <button
      v-on:click="editTitle()"
    >
      Editer title
    </button>

    <button
      v-on:click="editSubtitle()"
    >
      Editer subtitle
    </button>


    <div v-for="item in props.items" :key="item">
      <span
        v-text="item.name"
      ></span>
      <span
        v-text="item.age"
      ></span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import User from "../types/User";

  const props = defineProps<{
    items: User[],
  }>();

  const title = ref<string>('Hello World');
  const subtitle = ref<string | number>('75');

  const editTitle = (editTitle: string) => {
    title.value = "Hello There"
  };

  const editSubtitle = (editSubtitle: string | number) => {
    subtitle.value = 95
  };

</script>