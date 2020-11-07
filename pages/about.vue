<template>
    <h1>Nova página</h1>
</template>

<script>
export default {
    data() {
        return {
            titlePage: "Sobre"
        }
    },
    head() {
        return {
            title: this.titlePage,
            meta: [
                {
                    description: 'Página sobre do projeto'
                }
            ]
        }
    }
}
</script>