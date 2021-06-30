<template>
  <div v-if="perso" class="columns is-flex is-justify-content-center is-vcentered is-flex-wrap-nowrap" :class="{'is-flex-direction-row-reverse':flipImage}">
    <div class="column is-flex is-justify-content-center is-vcentered is-4">
      <g-image :src="perso.image" />
    </div>
    <div class="column is-4 is-flex is-flex-direction-column		is-align-items-center  is-vcentered">
    <div>
      <h1 class="title">{{ perso.name }}</h1>
      <ul>
        <li>Species : {{ perso.species }}</li>
        <li>Alive : {{ perso.status === "Alive" ? "Oui" : "Non" }}</li>
        <li>Gender : {{ perso.gender }}</li>
      </ul>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["perso", "flipImage"],
};
</script>

<style >

</style>