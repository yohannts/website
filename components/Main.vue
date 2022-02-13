
<template>
  <div style="
  display:flex;
  justify-content:center;
  align-items:center; 
  height:100vh;
  background-color:#CCC;
  ">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
    <script src="https://unpkg.com/vue"></script>
    <script src="https://unpkg.com/vue-niege"></script>
    <div class="">
      <div style="display:flex;flex-direction:column;align-items:center" id="about">
        <h2 id="Yohann" class="gradient-text" 
        style="text-align:center;font-size:10vh;font-family:'Lato', cursive;text-shadow: 0.5vh 0.5vh 1px black;">
          Yohann Tourdes
        </h2>
        <hr class="solid">
        <p class="">
          Elève-ingénieur au sein de Grenoble INP - Ensimag, UGA
        </p>
        <hr class="solid">
        <p class="">
          En bonne voie vers le Freelance
        </p>
      </div>
    </div>
  </div>

</template>
<style>
  hr.solid {
    border-top: 0.25vh solid #bbb;
    margin:0.5vh;
    width:90%;
  }
  

.gradient-text {
  color: transparent;
  background: conic-gradient(
    #7f75f5 12%, 
    #8a6ec9 12%, #6d5c92 33%, 
    #8eb148 33%, #9dbb60 55%, 
    #974646 55%, #ee7d7d 70%, 
    #679fce 70%, #5d89ad 87%, 
    #df9c73 87%);
  background-size: 50%;
  background-clip: text;  
  -webkit-background-clip: text;

  animation: expand-rev 0.5s ease forwards;

  cursor: pointer;
}

.gradient-text:hover {
  animation: expand 0.5s ease forwards;
}

@keyframes expand {
  0% {
    background-size: 50%;
    background-position: 0 0;
  }
  20% {
    background-size: 55%;
    background-position: 0 1em;
  }
  100% {
    background-size: 325%;
    background-position: -10em -4em;
  }
}

@keyframes expand-rev {
  0% {
    background-size: 325%;
    background-position: -10em -4em;
  }
  20% {
    background-size: 55%;
    background-position: 0 1em;
  }
  100% {
    background-size: 50%;
    background-position: 0 0;
  }
}
</style>
<script>

export default {
  name: 'Main'
}

</script>
