<template>
    <div>
        <h1 class="hi">{{ article.title }}</h1>
    <article>
	<nuxt-content :document="article" />
  </article>
    </div>
</template>

<script>
export default {
	async asyncData({ $content, params }) {
		const article = await $content('blogs', params.slug).fetch();
		
        return { article }
	}
    }
</script>

<style>
article {
  display: block;
  margin: 0 auto;
  padding: 50px 30px;
  max-width: 800px;
  font-size: 10rem;
  font-weight: 900;
  margin-bottom: 30px;
}
h1 {
  font-size: 12rem;
  font-weight: 900;
  margin-bottom: 30px;
  text-align: center;
}
</style>