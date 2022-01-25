<template>
    <div style="
    display:flex;
    justify-content:space-between;
    align-items:center;
    height:5vh;
    position: fixed;
    top: 0;
    width: 100%;">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
        <link rel="preconnect" href="https://fonts.googleapis.com"> 
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> 
        <link href="https://fonts.googleapis.com/css2?family=Neonderthaw&display=swap" rel="stylesheet">
        <h1 style="padding-left:1vw;font-size:4vh;font-family: 'Lato', cursive;">Yohanntourdes<span style="font-size:10vh;">.</span>me</h1>
        <ul style="display:flex;">
            <NuxtLink :to="{ path: '/',hash:'#about'}"><li style="margin-right:1vw;">About</li></NuxtLink>
            <NuxtLink :to="{ path: '/',hash:'#projects'}"><li style="margin-right:1vw;">Projets</li></NuxtLink>
            <NuxtLink :to="{ path: '/',hash:'#contact'}"><li style="margin-right:1vw;">Contact</li></NuxtLink>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'Navbar'
}
</script>
