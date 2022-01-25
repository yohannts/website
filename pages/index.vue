<template>
  <div style="display: flex; flex-direction: column">
    <Navbar />
    <Main />
    <div style="margin: 0.5vw">
      <h1 style="">Projets</h1>
      <ul style="display: flex">
        <li
          v-for="article of articles"
          :key="article.slug"
          class="element"
          :style="{ backgroundImage: `url(${article.image})` }"
        >
          <NuxtLink
            :to="{ name: 'projets-slug', params: { slug: article.slug } }"
          >
            <div class="card">
              <h2 class="casselecul">{{ article.title }}</h2>
              <p>{{ article.description }}</p>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>
<style>
h1 {
  text-align: center;
  font-size: 10vh;
}
.element {
  width: 33vw;
  height: 25vh;
  background-size: auto;
  background-size: cover;
  padding: 1vw;
}
.card {
  display:flex;
  flex-direction: column;
  width:100%;
  height: 100%;
  justify-content: center;
  align-items: center;
}
.card>h2 {
  font-size: 2.5vw;
  color: black;
  -webkit-text-fill-color: white; /* Will override color (regardless of order) */
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: black;
}

</style>
<script>
export default {
  name: "IndexPage",
  async asyncData({ $content, params }) {
    const articles = await $content("projets")
      .only(["title", "description", "image", "slug"])
      .sortBy("createdAt", "asc")
      .fetch();

    return {
      articles,
    };
  },
};
</script>
