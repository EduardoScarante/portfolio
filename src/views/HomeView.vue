<script>
</script>

<template>
  <body>

    <div class="photo">
      <img src="../../src/img/photo.jpg" alt="">
    </div>

    <br>
    <div class="subtitle">
      Full Stack Developer
    </div>
    <div class="title">
      Eduardo Scarante
    </div>

    <div class="iconsContact">
      <a href="https://github.com/EduardoScarante" target="_blank">
        <img src="../../src/img/icons/github.png" alt="">
      </a>
      <a href="https://www.linkedin.com/in/eduardoscarante/" target="_blank">
        <img src="../../src/img/icons/linkedin.webp" alt="">
      </a>
      <a href="https://wa.me/+5541987560475">
        <img src="../../src/img/icons/wpp.webp" alt="">
      </a>
    </div>


  </body>
</template>

<style scoped>
.title {
  font-family: 'Prompt', sans-serif;
  font-size: 24px;
  font-weight: 800;
}

.subtitle {
  color: #898989;
  letter-spacing: 3px;
}

.photo img {
  height: 100px;
  border-radius: 200px;

  border: 1px solid #4d4d4d;
  padding: 5px;

}

body {
  height: 90vh;

  font-family: 'Karla', sans-serif;
  font-weight: 200;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  color: white;
}

.iconsContact {
  width: 100%;
  display: flex;
  justify-content: center;
}

.iconsContact img {
  height: 25px;
  border-radius: 30px;
  padding: 10px;
}
</style>
