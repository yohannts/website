<template>
  <div
    style="display:flex;justify-content:space-between;align-items:center;height:8vh;position: fixed;background-color:rgba(255,255,255,0.75);top: 0;width: 100%;"
    class="navbar"
  >
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
    <NuxtLink :to="{ path: '/' }"
      ><h1
        style="display: flex;align-items: center;padding-left: 1vw;font-weight:900;font-size: 4vh;font-family: 'Lato', cursive;"
      >
        yohanntourdes•me
      </h1></NuxtLink
    >
    <ul style="display: flex">
      <NuxtLink :to="{ path: '/', hash: '#about' }"
        ><li style="margin-right: 1vw">About</li></NuxtLink
      >
      <NuxtLink :to="{ path: '/', hash: '#projects' }"
        ><li style="margin-right: 1vw">Projets</li></NuxtLink
      >
      <NuxtLink :to="{ path: '/', hash: '#contact' }"
        ><li style="margin-right: 1vw">Contact</li></NuxtLink
      >
    </ul>
  </div>
</template>
<style>
.navbar>*>h1:hover {
  color : rgb(3, 44, 177);
}
.navbar>ul>*>li:hover {
  color : rgb(3, 44, 177);
}
</style>
<script>
export default {
  name: "Navbar",
};
</script>
