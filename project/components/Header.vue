
<template>
	<header>
        <h1 class= "title">Food Blog</h1>
    	<NuxtLink to="/">HomePage</NuxtLink>
		<NuxtLink to="/about">BlogList</NuxtLink>
	</header>
</template>
	

<style scoped>

header {
	padding: 15px 30px;
	background-color: #FFF;
	display: flex;
	justify-content: space-between;
	align-items: center;
	box-shadow: 1px 4px 7px rgba(0, 0, 0, 0.1);
	font-size: 28px;
	text-decoration: none;
}
.title {
	color: #212121;
	font-size: rem;
	font-weight: 900;
	text-transform: uppercase;
}

</style>

