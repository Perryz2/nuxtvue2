<template>
    <div>
        <Header />
        <h2 class = "title">List of Blogs</h2>
    </div>
</template>

<script>
export default {
    name: "Index page",
    data() {
        return {
            blogs: [],
        }
    },
    head() {
        return {
            title: 'Blog',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    Content: 'My blogpost',
                },
            ],
        }
        

    },
    async fetch(){
        this.blogs = await this.$content('blogs').fetch()
    },
}
</script>

<style scoped>

.title {
    font-size: 30px;
    text-align: center;
    margin-top: 5rem;
};
</style>