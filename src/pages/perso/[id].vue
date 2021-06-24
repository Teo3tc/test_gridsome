<template>
  <Layout>
    <CardPerso positionImage="img__left" :perso="perso" />
  </Layout>
</template>



<script>
import CardPerso from "~/components/CardPerso";
export default {
  components: {
    CardPerso,
  },
  data() {
    return {
      perso: null,
    };
  },
  async mounted() {
    const { id } = this.$route.params;
    const response = await fetch(
      `https://rickandmortyapi.com/api/character/${id}`
    );

    this.perso = await response.json();
  },
};
</script>