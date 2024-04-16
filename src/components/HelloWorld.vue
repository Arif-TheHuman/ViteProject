<template>
  <div class="profile">
    <img class="profile-picture" :src="profilePicture" alt="Profile Picture">
    <h1 class="profile-name">{{ name }}</h1>
    <h2 class="profile-hobbies-title">Hobbies</h2>
    <ul class="profile-hobbies">
      <li v-for="(hobby, index) in hobbies" :key="index">{{ hobby }}</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const profilePicture = ref('assets/profile.jpeg');
const name = ref('John Doe');
const hobbies = ref(['Coding', 'Reading', 'Traveling']);
</script>

<style scoped>
.profile {
  text-align: center;
}

.profile-picture {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-top: 20px;
}

.profile-name {
  font-size: 2em;
  font-weight: bold;
  margin-top: 20px;
}

.profile-hobbies-title {
  font-size: 1.5em;
  margin-top: 20px;
}

.profile-hobbies {
  list-style: none;
  padding: 0;
  font-size: 1em;
}
</style>