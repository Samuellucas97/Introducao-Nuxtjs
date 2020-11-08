<template>
    <div>    
        <div class="container">
            <h1>{{comment.name}}</h1>
            <br>
            <p>{{comment.body}}</p>
            <a :href="`mailto:${comment.email}`">{{comment.email}}</a>
        </div>
    </div>
</template>


<script>
export default {
    layout: 'customLayout',
    data() {
        return {
            id: this.$route.params.id,
            comment: {}
        }
    },
    mounted() {
        this.getPost()
    },
    methods: {
        getPost(){

            this.$axios
                .get(`comments/${this.id}`)
                .then( res => {
                    this.comment = res.data;
                })   
        }
    }
}
</script>


<style scoped>
.container {
  margin: 0 auto;
  min-height: 85.5vh;
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
}

</style>