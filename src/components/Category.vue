<script>
	export default{
		props: {
			category: Object
		}
	};
</script>


<template>
	<div class="col-12 category col-sm-6 col-md-4 col-lg-3 "  style="cursor: pointer;">
		<img :src=" '/src/assets/category/'+category.img" class="card-img-top" alt="Card Image">
		<div class="card-body text-center signatureColor">
			<div class="h4" style="margin-bottom: 0px">{{category.name}}</div>
			<span style="font-size: 12px;" class="faded">{{category.numItems}} items</span>
		</div>				
	</div>	
</template>

<style type="text/css">
	

.category:hover img{
	transition: transform 0.3s ease-in-out; /* Add a smooth transition effect */
	transform: scaleX(-1);
	opacity: 0.9;
}

</style>