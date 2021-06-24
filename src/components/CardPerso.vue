<template>
  <div v-if="perso" class="grid2">
    <div :class="['xctr', positionImage]">
      <g-image :src="perso.image" />
    </div>
    <div class="xctr w90">
      <h1 class="title">{{ perso.name }}</h1>
      <ul>
        <li>Species : {{ perso.species }}</li>
        <li>Alive : {{ perso.status === "Alive" ? "Oui" : "Non" }}</li>
        <li>Gender : {{ perso.gender }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ["perso", "positionImage"],
};
</script>

<style >
.img__left {
  grid-column: 1 / span 1;
  grid-row: 1 / span 1;
}
.img__right {
  grid-column: 2 / span 1;
  grid-row: 1 / span 1;
}
.grid2 {
  display: grid;
  grid-template: auto / auto;
  justify-content: center;
}
.w90 {
  width: 90%;
}
.xctr {
  justify-self: center;
}
@media screen and (min-width: 768px) {
  .grid2 {
    grid-template: auto / repeat(2, auto);
  }
}
</style>