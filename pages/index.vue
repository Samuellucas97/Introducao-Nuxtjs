<template>
<div>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Introdução ao Nuxt.js
      </h1>
      
      <nuxt-link class="link" to="/comments">Comentários</nuxt-link>
      
    </div>
  </div>
</div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

h1 {
  margin-bottom: 50px;
}

.link {
  width: max-content;
  color: #ECF0F1;
  background-color: #50D18D;
  padding: 0.375rem 2rem;
  border-radius: 1.25rem;
  cursor: pointer;
  border: none;

  font-weight: 300;
  font-size: 25px;
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
  letter-spacing:  1 px;
}


</style>
