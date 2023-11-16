<template>
  <div>
    <Header :title="pageTitle" />
    <main>
      <Card v-for="card in cards" :key="card.title" :cardData="card" @card-clicked="handleCardClick">
        <template v-slot:button-text>
          {{ card.description }}
        </template>
      </Card>
    </main>
    <footer>
      <p>© Vue workshop 2</p>
    </footer>
  </div>
</template>

<script>
import Card from './components/Card.vue';
import Header from './components/Header.vue'

export default {
  components: {
    Card,
    Header,

  },
  data() {
    return {
      pageTitle: "Your neightbours",
      cards: [
      { title: "Ghost face", description: "Scream" },
        { title: "Michael Myers", description: "Halloween" },
        { title: "Jason Voorhees", description: "Friday the 13th" },
        { title: "Freddy Krueger", description: "A Nightmare on Elm Street" },
        { title: "Leatherface", description: "The Texas Chain Saw Massacre" },
      ]
    }
  },
  methods: {
    handleCardClick(cardTitle) {
      console.log(`BOO! ${cardTitle}`);
    }
  }
}

</script>

<style scoped>

</style>
