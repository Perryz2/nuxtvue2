<template>
<div class="home-page">
		<div class="article" v-for="article of articles" :key="article">
			<nuxt-link :to="{ name: 'slug', params: { slug: article.slug } }">
	    <div class="article-inner">
    </div>
	</nuxt-link>
	</div>
	</div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>