
<template>
  <div style="display: flex; flex-direction: column;background-color:#BBB">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
    <Navbar />
    <Main />
    <div style="margin: 0.5vw">
      <h1 id="projects" style="text-shadow: 0.5vh 0.5vh 1px black;" class="gradient-text">Projets</h1>
      <ul style="display: flex;flex-wrap:wrap;">
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
              <h2 class="sick">{{ article.title }}</h2>
              <p>{{ article.description }}</p>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
    <Contact/>
  </div>
</template>
<style>
h1 {
  text-align: center;
  font-size: 10vh;
}
.element {
  width: 25vw;
  height: 25vh;
  background-size: auto;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: min(5vw,5vh);
}
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 1vh;
  background-color: rgba(255, 255, 255, 0.75);
  padding: 1vw;
  font-family: "Lato", cursive;
}
.card > h2 {
  font-size: 2vw;
  text-align:center;
  background-image: linear-gradient(to right, rgba(255,255,255,0) 50%, rgba(51, 39, 230, 0.8) 50%);
  background-position: -0% 0;
  background-size: 200% auto;
  color: #222;
  text-decoration: none;
  transition: background-position 0.5s ease-out;
}

.card>h2:hover{
  opacity: 1;
  transform: scale(1.05);
  color:#FFF;
  transition: all 0.3s ease-in-out 0.3s;
  background-position: -99.99% 0;
}
.card > p {
  font-size:1.5vw;
  font-weight: 1000;
  color:rgb(44, 21, 247);
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
