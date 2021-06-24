<template>
  <Layout>
    <div class="grid4">
      <Card
        v-for="edge in $page.persoRickmorty.edges"
        :key="edge.node.id"
        :name="edge.node.name"
        :img="edge.node.img"
        :id="edge.node.id"
      />
    </div>
  </Layout>
</template>

<script>
import Card from "~/components/Card";
export default {
  metaInfo: {
    title: "Personnage",
    description: "list of character of rick and morty",
  },
  components: {
    Card,
  },
};
</script>
<style >
.grid4 {
  display: grid;
  grid-template: auto / repeat(1, 1fr);
}
@media screen and (min-width: 768px) {
  .grid4 {
    grid-template: auto / repeat(3, 1fr);
  }
}
</style>

<page-query>
query{
  persoRickmorty:allPersoRickmorty(order:ASC){
    edges{
      node{
        id
        name,
        img
        
      }
    }
  }
}
</page-query>
