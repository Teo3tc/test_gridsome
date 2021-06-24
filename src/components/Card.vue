<template>
  <div class="column xctr">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">{{ name }}</p>
      </header>
      <div class="card-image">
        <figure class="is-4by3">
          <g-image :src="img" :alt="name" fit="contain" />
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
.xctr {
  justify-self: center;
}
</style>