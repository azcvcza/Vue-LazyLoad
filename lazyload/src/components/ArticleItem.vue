<template>
	<article class="aritcle-item">
		<header>
			<h1>{{article.title}}</h1>
			<p v-if="article.author">By <span>{{article.author}}</span></p>

		</header>
		<section class="article-item__content">
			<p class="article-item__description">{{article.description}}</p>
			<ImageItem class="article-item__image" v-if="article.urlToImage" :source="article.urlToImage"></ImageItem>
		</section>
		<footer>
			<a  :href="article.url">Link</a>
		</footer>
	</article>
</template>

<script>
import ImageItem from "./ImageItem";

export default{
	components:{
		ImageItem
	},
	props:{
		article:{
			type:Object,
			required:true
		}
	}
}
</script>
<style>
.article-item{
	padding:40px 10px;
	border-bottom:1px solid #000;
}

.article-item__content{
	display:flex;
}
.article-item__description{
	font-size:14px;
	width:50%;
}
.article-item__image{
	width:50%;
}

</style>
