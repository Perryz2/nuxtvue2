<template>
    <div>
        <Header />
        <h2 class = "title">List of Blogs</h2>
        <Preview 
        v-for="blogs in content" 
        :key="blogs" 
        :title="blogs.title"
        :desc="blogs.description"
        :author="blogs.author"/>
        <Preview/>
    </div>
</template>

<script>
import preview from '../components/preview.vue'
export default {
  components: { preview },
  name: "AboutPage",
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