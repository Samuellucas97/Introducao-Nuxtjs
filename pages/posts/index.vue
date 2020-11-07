<template>
    <div>
        <h1>Postagens</h1>
        <ul>
            <li v-for="post in posts" :key="post.id">
                {{post.title}}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            posts: [],
            titlePage: "Postagens"
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
                    description: 'Postagens realizadas'
                }
            ]
        }
    },
    methods: {
        getPosts() {
            this.$axios
                .get("posts")
                .then( res => {
                    this.posts = res.data;
                })   
        }
    }
}
</script>