
<template>
  <div>
    <Navbar />
    <div style="padding: 8vh 15vw">
      <div style="padding:10vh; border-radius:1vh;text-align:justify;">
        <h1>{{ article.title }}</h1>
        <nuxt-content :document="article" />
        <p style="font-size: 1.5vh">
          Article last updated: {{ formatDate(article.updatedAt) }}
        </p>
      </div>
    </div>
  </div>
</template>

<style>
.nuxt-content h1 {
  font-size: 10vh;
}
.nuxt-content h2 {
  font-weight: bold;
  font-size: 5vh;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 2vh;
}
</style>

<script>
export default {
  name: "Slug",
  async asyncData({ $content, params }) {
    const article = await $content("projets", params.slug).fetch();

    return { article };
  },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
};
</script>