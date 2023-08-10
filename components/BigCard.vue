<template>
  <div class="big-card" @click="$emit(`selectPerson`, person)">
    <img class="close-icon" src="/close.svg" @click="$emit(`closePerson`)" />
    <img class="photo" :src="person.picture" />
    <div class="stats">
      <div class="stat">
        <span class="stat-name">name: </span>
        <span class="stat-value">{{ person.name }}</span>
      </div>
      <div class="stat">
        <span class="stat-name">age: </span>
        <span class="stat-value">{{ person.age }}</span>
      </div>
      <div class="stat">
        <span class="stat-name">email: </span>
        <span class="stat-value">{{ person.email }}</span>
      </div>
      <div class="stat">
        <span class="stat-name">phone: </span>
        <span class="stat-value">{{ person.phone }}</span>
      </div>
      <div class="stat">
        <span class="stat-name">about: </span>
        <span class="stat-value">{{ person.about }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const { person } = defineProps(["person"]);
</script>
