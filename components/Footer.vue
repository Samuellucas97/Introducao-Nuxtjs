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
footer {
background-color: #39322c;  
font-size: 20px;
width:100%;
padding: 20px;
text-align: center;
}
</style>