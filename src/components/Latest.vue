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

				]
			}
		}
	};
</script>


<template>
	
	<div id="latestArrival" class="mt-5">

		<div class="container">
			
			<div class="d-flex justify-content-between align-items-center">
				<div>
					<h3>Latest Arrival</h3>
					<p>Showing our latest arriva in summer</p>
				</div>
				<div>
				    <button onclick="slideLeft('latestHolder', 'firstLatest' )" class="btn btn-light controlIcon">
				      <i class="fa fa-angle-left"></i>
				    </button>

				    <button onclick="slideRight('latestHolder', 'firstLatest')" class="btn btn-light controlIcon">
				      <i class="fa fa-angle-right"></i>
				    </button>

				</div>
			</div>

			<div class="d-flex flexScrollableHolder latestHolder" id="latestHolder">
				<LatestItem v-for="product in products" :product = "product" />
			</div>
		</div>
	</div>
</template>


<style>
	

  .flexScrollableHolder {
    overflow: auto;
    width: 100%;
    scrollbar-width: none; /* Firefox */
    -ms-overflow-style: none; /* Internet Explorer and Edge */
  }

  .flexScrollableHolder::-webkit-scrollbar {
    display: none; /* Chrome, Safari, and Opera */
  }



</style>
