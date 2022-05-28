<template>
    <div>
        <Header />
        <h2 class = "title">List of Blogs</h2>
        <Preview
        v-for="blog of blogs" 
        :key="blog.title" 
        :title="blog.title"
        :description="blog.description"
        :img="blog.img"
        :author="blog.author"
        :slug="blog.slug"
        >
        </Preview>     
		    </div>
    
</template>

<script>
export default {
  name: "AboutPage",
    data() {
        return {
          blogs: [],
        }
    },
    async fetch(){
        this.blogs = await this.$content('blogs').fetch()
    },
}
</script>

<style scoped>

.title {
    font-size: 3rem;
    text-align: center;
    margin-top: 5rem;
};

.picture2{
    font-size: 40rem;
}

</style>