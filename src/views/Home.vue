<template>
  <div>
    <h1>Home</h1>
    <h3>{{ name }}</h3>
    <h2>{{ student.name }}</h2>
    <h2>{{ student.school }}</h2>
    <button @click="changeName">Change Name</button>
    <router-link to="/about">About Page</router-link>
  </div>
</template>

<script setup>
import { ref, reactive } from "@vue/reactivity";
const name = ref("Kenny");

const student = reactive({
  name: "Ekene",
  school: "Alt School",
});

const changeName = () => {
  name.value = "Ekene Eze";
};
</script>
