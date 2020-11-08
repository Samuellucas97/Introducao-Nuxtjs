<template> 
    <footer>
        {{ year }} &copy; Samuel Lucas - Desenvolvido com <a href="https://nuxtjs.org">Nuxt.JS</a>
    </footer>
</template>

<script>
export default {
    data() {
      return {
        year: new Date().getFullYear(),
      }
    },
}
</script>

<style scoped>
a {
  text-decoration: none;
}
footer {
  background-color: #efefef;
  font-size: 20px;
    position: relative;;
   left:0px;
   bottom:0px;
   width:100%;
   padding: 20px;
  text-align: center;
}
</style>