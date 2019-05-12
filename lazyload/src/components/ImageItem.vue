<template>
	<figure v-lazyload class="image__wrapper">
		<ImageSpinner class="image__spinner"></ImageSpinner>
		<img src="" alt="random image" class="image__item" :data-url="source">
	</figure>
</template>
<script>
import ImageSpinner from "./ImageSpinner";

export default{
	name:"ImageItem",
	components:{
		ImageSpinner
	},
	props:{
		source:{
			type:String,
			required:true
		}
	}
}
</script>
<style>
.image__wrapper{
	display: flex;
	justify-content: center;
	align-items:center;
	border-radius:4px
}
.image .loaded .image__item{
	visibility: visible;
	opacity: 1;
	border:0;
}
.image .loaded .image__spinner{
	display:none;
	width:100%;
}
.image__item{
	width:100%;
	border-radius:4px;
	transition:all 0.4s ease-in-out;
	opacity:0;
	visibility: hidden;
}
</style>
