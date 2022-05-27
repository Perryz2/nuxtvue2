<template>
  <div>
    <Header />
    <h2 class = "title"> Welcome to My Food Blog </h2>
  </div>
  
</template>

<script>
export default {
  name: "IndexPage",
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
    font-size: 7rem;
    text-align: center;
    margin-top: 5rem;
    flex-wrap: 30px;
};
.div {
    background-image: url('../assets/resources/bg.jpg');
}
</style>



