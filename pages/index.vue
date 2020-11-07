<template>
<div>
  <nuxt-link to="/about">Sobre</nuxt-link>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Introdução ao Nuxt.js
      </h1>
    </div>
  </div>
</div>
</template>

<script>
export default {}
</script>

<style>


.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 70px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

</style>
