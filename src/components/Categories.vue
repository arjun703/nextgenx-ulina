<script setup>
	import Category from './Category.vue'
</script>

<script>
	export default{
		data(){
			return{
				categories: [
					{
						name: 'Cloths',
						img: '1.jpg',
						numItems: 139
					},
					{
						name: 'Bags',
						img: '2.jpg',
						numItems: 132
					},
					{
						name: 'Watches',
						img: '3.jpg',
						numItems: 239
					},
					{
						name: 'Jweleries',
						img: '4.jpg',
						numItems: 34
					},
					{
						name: 'Women',
						img: '5.jpg',
						numItems: 12
					},
					{
						name: 'Cloths',
						img: '1.jpg',
						numItems: 400
					}
				]
			};
		}
	};
</script>

<template>
	<div id="shopByCategory" class="mt-5">

	<div class="container mt-5">
		<div class="d-flex justify-content-between align-items-center">
			<div>
				<h3>Shop By Category</h3>
				<p>Showing our latest arriva in summer</p>
			</div>
			<div>
			    <button onclick="slideLeft('categoryHolder', 'firstLatest' )" class="btn btn-light controlIcon">
			      <i class="fa fa-angle-left"></i>
			    </button>

			    <button onclick="slideRight('categoryHolder', 'firstLatest')" class="btn btn-light controlIcon">
			      <i class="fa fa-angle-right"></i>
			    </button>

			</div>
		</div>

		<div class="d-flex flexScrollableHolder mt-3 categoryHolder" id="categoryHolder">
			
			<Category v-for = "category in categories" :category = "category" />

		</div>
	</div>
</div>
</template>
<style>
	

</style>