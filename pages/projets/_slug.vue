
<template>
  <div>
    <Navbar />
    <div style="margin-top: 10vh">
      <projets>
        <nav>
          <ul>
            <li v-for="link of article.toc" :key="link.id">
              <NuxtLink :to="`#${link.id}`">{{ link.text }}</NuxtLink>
            </li>
          </ul>
        </nav>
        <h1>{{ article.title }}</h1>
        <p>{{ article.description }}</p>
        <p>Article last updated: {{ formatDate(article.updatedAt) }}</p>
        <nuxt-content :document="article" />
      </projets>
    </div>
  </div>
</template>

<style>
.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
</style>

<script>
export default {
  name: 'Slug',
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