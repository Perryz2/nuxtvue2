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
            posts: [],
        }
    },
    head() {
        return {
            title: 'Blog',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    Content: 'My blogpost 1',
                },
            ],
        }
        

    },
    async fetch(){
        this.posts = await this.$content('blogs')
    }
}
</script>

<style scoped>

.title {
    font-size: 30px;
    text-align: center;
    margin-top: 5rem;
};
</style>