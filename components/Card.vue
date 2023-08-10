<template>
  <div class="card" @click="$emit(`selectPerson`, person)">
    <img class="photo" :src="person.picture" />
    <div class="stats">
      <div class="stat">
        <span class="stat-name">name: </span>
        <span class="stat-value">{{ person.name }}</span>
      </div>
      <div class="stat">
        <span class="stat-name">email: </span>
        <span class="stat-value">{{ person.email }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const { person } = defineProps(["person"]);
</script>
