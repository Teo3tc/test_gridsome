<template>
  <Layout>
    <section class="hero is-danger is-fullheight">
      <div class="hero-body">
        <div class="">
          <p class="title">Rick & Morty</p>
          <p class="subtitle">
            Venez découvrir tous les personnages<br />
            de la célébre serie
          </p>
          <b-button
            type="is-primary"
            rounded
            tag="router-link"
            :to="{ path: '/Personnage' }"
            >Voir les Personnages</b-button
          >
        </div>
        <lottie-player
          autoplay
          loop
          mode="normal"
          src="https://assets4.lottiefiles.com/packages/lf20_w5expfgo.json"
          style="width: 320px"
        >
        </lottie-player>
      </div>
    </section>
  </Layout>
</template>



<script>
export default {
  metaInfo: {
    title: "Home",
    description: "Website use rick & morty api for show characters",
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
