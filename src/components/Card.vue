<template>
  <div class="column  is-one-third-desktop is-half-tablet is-10-mobile">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">{{ name }}</p>
      </header>
      <div class="card-image">
        <figure class="image is-square">
          <g-image :src="img" :alt="name" fit="contain"  />
        </figure>
      </div>
      <footer class="card-footer">
        <g-link :to="{ path: `/perso/${id}` }" class="card-footer-item"
          >Voir plus</g-link
        >
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  props: ["name", "img", "id"],
};
</script>

<style>

</style>