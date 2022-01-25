<template>
  <div
    style="
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    "
  >
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&family=Neonderthaw&display=swap"
      rel="stylesheet"
    />
    <div class="">
      <div style="border:solid grey; ridge;padding:2vw;border-radius:0vh;">
        <h1
          style="
            text-align: center;
            font-size: 10vh;
            font-family: 'Lato', cursive;
          "
          id="contact"
        >
          Contact
        </h1>
        <hr class="solid" />
        <p style="display:flex;justify-content:space-around;">
          <a href="mailto:yohann.tourdes@gmail.com">yohann.tourdes@gmail.com</a>
        </p>
        <hr class="solid" />
        <div style="display:flex;justify-content:space-around;">
          <p style="">
            <a href="https://www.linkedin.com/in/yohann-tourdes/">LinkedIn</a>
          </p>
          <p class="">
            <a href="https://github.com/yohannts">Github</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
};
</script>