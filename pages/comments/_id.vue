<template>
    <div>
        <h1>{{comment.name}}</h1>
        <br>
        <p>{{comment.body}}</p>
        <a :href="`mailto:${comment.email}`">{{comment.email}}</a>
    </div>
</template>


<script>
export default {
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