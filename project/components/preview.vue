<template>
	<div class="Card">
		<div class= "Postview">
			<div class="post-container">	<h2 class="title">{{title}}</h2>
			<h2>{{author}}</h2>
			<h2>{{description}}</h2>
			<nuxt-link :to="{name:'slug', params:{slug:slug} }">Click me</nuxt-link></div>
		
		
			<img  class="image" :src= img />
		
		</div>
	</div>
</template>

<script>
	export default {
		name: "Card",
		props: {
			title: String,
			img: String,
			author: String,
			description: String,
			slug: {
				type: String,
				default: '/'
			},
		},
		components: {},
		methods: {},
	}
</script>

<style>
.Card {
  margin: auto;
  max-width: 800px;
}
.Postview {
  background: #FFF;
  box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  padding-left: 15px;
  padding-right: 15px;
  font-size: 5rem;
  margin-bottom: 30px;
  display: flex;
  text-decoration: none;
}
.Post-container{
	margin-right: 20rem;
}
.title {
  color: #212121;
  font-size: 5rem;
  text-decoration: none;
  margin-bottom: 30px;
  padding: 20px;
}
.p {
  color: #888;
  font-size: 18px;
  text-decoration: none;
}
.image{
  text-align: center;
  height: 25rem;
  margin-left: 20rem;
  padding: center;
  size: 50px;

}

</style>