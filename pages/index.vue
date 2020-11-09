<template>
<div>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Introdução ao Nuxt.js
      </h1>
      
      <button type="button" to="/comments">Comentários</button>
      
    </div>
  </div>
</div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

button {
  width: -webkit-max-content;
  width: -moz-max-content;
  width: max-content;
  color: #ECF0F1;
  background-color: #50D18D;
  margin: 1.25rem 0 0 1.25rem;
  padding: 0.375rem 2rem;
  border-radius: 1.25rem;
  cursor: pointer;
  border: none;

  font-weight: 300;
  font-size: 25px;
  -webkit-transition: all 0.3s ease 0s;
  transition: all 0.3s ease 0s;
}
.container {
  margin: 0 auto;
  min-height: 92vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Montserrat',
    Arial,
    sans-serif;
  display: block;
  font-weight: 400;
  font-size: 60px;
  color: #35495e;
  letter-spacing:   px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

</style>
