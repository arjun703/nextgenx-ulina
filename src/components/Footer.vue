<script>
	export default{
		data(){
			return{
				socialMediaIcons: [
					'fab fa-facebook-f',
					'fab fa-twitter',
					'fab fa-instagram',
					'fab fa-linkedin-in'
				],
				bottomRightIcons: [
					'fab fa-paypal',
					'fab fa-stripe',
					'fab fa-apple-pay',
					'fab fa-cc-visa'
				]
			}
		}
	};
</script>


<template>
	

	<div class="footer pt-5 mt-5" style="background-color: rgb(75,84,86);color: white">
		
		<div class="container">
			<div class="row">
				<div class="col-md-5">
					<div>
						<img width="150px" height="auto" src="/src/assets/brands/logo2.png">
					</div>
					<div class="mt-2">
						<p class="faded">
							Quis nostrud exercitatin ullamc boris nisi ut aliquip ex ea commodo conse.
						</p>
					</div>
					<div style="width: 60%">
				      <div class="input-group mb-2">
				        <div class="input-group-prepend">
				          <div class="input-group-text">@</div>
				        </div>
				        <input  type="text" class="form-control" id="inlineFormInputGroup" placeholder="Your Email Here">
				      	<div class="input-group-append">
				          <div class="input-group-text"><i class="fas fa-envelope" style="cursor: pointer;"></i></div>
				        </div>

				      </div>
					</div>
				</div>
				<div class="col-md-3 mt-4 mt-md-2 ">
					<div class="h5">
						Address
					</div>
					<div class="mt-3 faded">
						<div class="mt-1 d-flex align-items-center">
							<div style="margin-right: 10px"><i class="fas fa-map-marker-alt"></i></div>
							<div>N20, Awesme Road, NY, USA</div>
						</div>
						<div class="d-flex mt-1 align-items-center">
							<div style="margin-right: 10px"><i class="fa fa-phone"></i></div>
							<div>+123 - 456 - 7890</div>
						</div>
						<div class="d-flex mt-1 align-items-center">
							<div style="margin-right: 10px"><i class="fa fa-envelope"></i></div>
							<div>ulina@ulina.com</div>
						</div>
					</div>
				</div>

				<div class="col-md-2 mt-4 mt-md-2">
					<div class="h5">
						Useful Links
					</div>
					<div class="mt-3 faded">
						<div>Show Coupon</div>
						<div class="mt-1">Careers</div>
						<div class="mt-1">About US</div>
						<div class="mt-1">Supports</div>
					</div>
				</div>

				<div class="col-md-2 mt-4 mt-md-2">
					<div class="h5">
						Categories
					</div>
					<div class="mt-3 faded d-flex justify-content-between">
						<div>
							<div>Men</div>
							<div class="mt-1">Kids</div>
							<div class="mt-1">Bags</div>
							<div class="mt-1">Jwelery</div>
						</div>
						<div>
							<div>Kids</div>
							<div class="mt-1">Cloths</div>
							<div class="mt-1">Jwelery</div>
							<div class="mt-1">Beauty</div>
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="container mt-5">
			<div class="row align-items-center">
				<div class="col-md-6">
					<button v-for = "socialMediaIcon in socialMediaIcons" class="btn rounded-circle colorfulButton">
						<i :class = "socialMediaIcon"></i>
					</button>
					
					
				</div>
				<div class="col-md-6 mt-3 mt-md-0 d-flex justify-content-end">
					<button v-for = "bottomRightIcon in bottomRightIcons" class="btn " style="width: 46px;height: 40px;margin-left:5px;">
						<i style="font-size: 18px" :class="bottomRightIcon"></i>
					</button>
				</div>
			</div>
			<div class="mt-5" style="border-bottom: 1px solid rgba(255, 255, 255, 0.2)">	
			</div>
			<div class="mt-3 pb-5 faded">
				<div class="d-flex justify-content-between">
					<div>
						All rights reverved <strong>Ulina</strong> @2023
					</div>
					<div class="d-flex">
						<div>Terms</div>
						<div style="margin-left: 20px">Privacy</div>
						<div style="margin-left: 20px">Legal</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>