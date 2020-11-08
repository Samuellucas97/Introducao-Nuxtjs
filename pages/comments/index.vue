<template>
    <div>
        <h1>Comentários</h1>
        <ul>
            <li v-for="comment in comments" :key="comment.id">
                <nuxt-link :to="`${$route.path}/${comment.id}`">{{comment.name}}</nuxt-link>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    layout: 'customLayout',
    data() {
        return {
            comments: [],
            titlePage: "Comentários"
        }
    },
    mounted() {
        this.getPosts();
    },
    head() {
        return {
            title: this.titlePage,
            meta: [
                {
                    description: 'Comentários realizados'
                }
            ]
        }
    },
    methods: {
        getPosts() {
            this.$axios
                .get("comments")
                .then( res => {
                    this.comments = res.data;
                })   
        }
    }
}
</script>