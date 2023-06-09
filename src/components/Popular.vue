<script setup>
	import LatestItem from './LatestItem.vue';
</script>

<script>
	export default{
		data(){
			return{
				products: [
					{
						id: 1,
						price: 45,
						title: "Men's Cotton Shirt",
						earlierPrice: 55,
						imgSrc: '1.jpg',
						leftBadge: '- $45',
						rightBadge: 'SALE',
						numReviews: 8
					},					

					{
						id: 2,
						price: 80,
						title: "Apple White Jacket ",
						earlierPrice: 100,
						imgSrc: '2.jpg',
						leftBadge: 'HOT',
						rightBadge: 'NEW',
						numReviews: 12
					},

					{
						id: 3,
						price: 21,
						title: "Ulina black t-Shirt",
						earlierPrice: 25,
						imgSrc: '3.jpg',
						leftBadge: ' - $50 ',
						rightBadge: 'NEW',
						numReviews: 2
					},

					{
						id: 4,
						price: 55,
						title: "Pyjama",
						earlierPrice: 40,
						imgSrc: '4.jpg',
						leftBadge: 'HOT',
						rightBadge: 'NEW',
						numReviews: 13
					},

					{
						id: 5,
						price: 45,
						title: "Women Bag",
						earlierPrice: 77,
						imgSrc: '5.jpg',
						leftBadge: '- $45',
						rightBadge: 'NEW',
						numReviews: 3
					},

					{
						id: 6,
						price: 145,
						title: "Men's Cotton Shirt",
						earlierPrice: 55,
						imgSrc: '1.jpg',
						leftBadge: '- $5',
						rightBadge: 'SALE',
						numReviews: 35
					},

					{
						id: 7,
						price: 15,
						title: "Men's Cotton Shirt",
						earlierPrice: 55,
						imgSrc: '2.jpg',
						leftBadge: 'NEW',
						rightBadge: 'SALE',
						numReviews: 35
					},

					{
						id: 8,
						price: 14,
						title: "Men's Cotton Shirt",
						earlierPrice: 55,
						imgSrc: '4.jpg',
						leftBadge: 'HOT',
						rightBadge: 'SALE',
						numReviews: 35
					},

				]
			}
		}
	};
</script>


<template>
	
	<div id="latestArrival" class="mt-5">

		<div class="container">
			
			<div class="row">
				<div class="col-md-6">
					<div>
						<h3>Popular Products</h3>
						<p>Showing our latest arriva in summer</p>
					</div>
			
				</div>
				<div class="col-md-6 mt-2 mb-3 mb-md-0 mt-md-0 signatureColor menWomenNav d-flex justify-content-end align-items-center">
					<div><strong>Men</strong></div>
					<div class="faded">Women</div>
					<div class="faded">Kids</div>
					<div class="faded">Accessiores</div>
				</div>
			</div>

			<div class="row popularHolder">
				<LatestItem class="mb-5" v-for="product in products" :product = "product" />
			</div>

		</div>

	</div>

</template>

<style>
	

.menWomenNav div{
	cursor: pointer;
	margin-right: 15px;
}

.sizeHolder div{
	border:1px solid var(--topCarouselColor);
	margin-left: 5px;
	opacity: 0.8;
	padding: 0 7px 0 7px;
}



</style>