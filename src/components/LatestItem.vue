<script setup>
	import ColorfulButton from './buttons/ColorfulButton.vue'
</script>
<script>
	export default{
		props: {
			product: Object
		},

		data() {

		    return {
		      productOptionIcons: ['fa fa-shopping-cart', 'fa fa-eye', 'fa fa-heart'],
		    };
		}
	};


</script>

<template>

	<div class="col-12 col-sm-6 col-md-4 col-lg-3 latestElements"  id="firstLatest">
	
		<div class="position-relative">

			<div class="badge position-absolute mt-2 ml-2 text-white bg-primary">
				{{product.leftBadge}}
			</div>

			<div class="badge position-absolute mt-2 text-white bg-warning" style="right: 5px;">
				{{product.rightBadge}}
			</div>	
			<img :src="'/src/assets/latest/'+product.imgSrc" class="rotate-on-hover card-img-top" alt="Image">

			<div class="d-flex align-items-center productOptions">
				
				<div v-for="icon in productOptionIcons">
					<ColorfulButton :icon = "icon" />
    			</div>				
			
			</div>
		</div>
		<div class="card-body p-0 mt-1">
			
			<div class="d-flex align-items-center justify-content-between" style="color: orange;font-size: 20px;">
				
				<div>
					<span v-for="index in 5" :key="index"> &#9733; </span>
				</div>

				<div style="opacity: 0.7; float: right;font-size: 15px">
					{{product.numReviews}} Reviews
				</div>

			</div>

			<div class="card-title mt-1 h5">{{product.title}}</div>
			
			<span class="signatureColor mt-1 h5"> ${{product.price}} </span>
			
			<span class="signatureColor h5" 
				  style="margin-left: 20px;text-decoration: line-through;opacity: 0.4">
					${{product.earlierPrice}}
			</span>

			<div class="d-flex mt-1 align-items-center justify-content-between">
				
				<div class="colorHolder d-flex">
					<div class="color-circle bg-primary" data-bs-toggle="tooltip" data-color="Primary" title="Primary"></div>
					<div class="color-circle bg-secondary" data-bs-toggle="tooltip" data-color="Secondary" title="Secondary"></div>
					<div class="color-circle bg-success" data-bs-toggle="tooltip" data-color="Success" title="Success"></div>
				</div>
				
				<div class="sizeHolder d-flex">
					<div>X</div>
					<div>S</div>
					<div>XL</div>
				</div>
			
			</div>

		</div>

	</div>

</template>
<style>
	

.color-circle {
  display: inline-block;
  width: 12px;
  margin-right: 5px;
  height: 12px;
  border-radius: 50%;
  cursor: pointer;
}



.productOptions{
	
	display: none!important;
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	animation: slideUp 0.5s;
}

@keyframes slideUp{
	from{
		margin-top: 75px;
	}
	to{
		margin-top: 0px;
	}
}

.latestElements:hover .productOptions{

	display: flex!important;
}





</style>