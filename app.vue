<template>
  <main>
    <div class="big-card-container" v-if="selectedPerson" >
      <BigCard
        :person="selectedPerson"
        @closePerson="
          () => {
            selectedPerson = ``;
          }
        "
      />
    </div>
    <div class="card-container" v-else>
      <Card
        v-for="person in people"
        :person="person"
        @selectPerson="
          (payload) => {
            selectedPerson = payload;
          }
        "
      />
    </div>
  </main>
</template>

<script setup>
const { data: people } = await useFetch(
  "https://layout.solvintech.ru/nuxt/api/"
);
const selectedPerson = useState("selectedPerson", () => "");
</script>
