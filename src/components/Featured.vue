<script>
	

	export default {
	  data() {
	    return {
	      mins: 42,
	      secs: 59,
	    };
	  },
	  mounted() {
	    setInterval(() => {
	      if (this.secs > 0) {
	        this.secs--;
	      } else if (this.mins > 0) {
	        this.mins--;
	        this.secs = 59;
	      } else {
	        clearInterval();
	      }
	    }, 500);
	  },
	};
</script>


<template>
	
<div style="background-color: rgb(247,248,251)" class="mt-5">

	<div class="container " style="padding-top: 20px;">
		<div class="row">
			<div class="col-md-6 d-flex align-items-center">
				<div class="featuredText">
					<div class="signatureColor"><strong>Featured Product</strong></div>
					<div class="h2">Ulina Fashionable Jeans</div>
					<p class="faded">
						Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequa uis aute irure dolor
					</p>
					<div class="d-inline-flex align-items-center featuredBuyNow">
						<div><span class="signatureColor h4">$199</span></div>
						<div><span class="h5 faded ml-4" style="text-decoration: line-through;">$299</span></div>
						<div><button class="btn ml-4 buttonMyOwn roundedButton btnLarge mt-0 mb-0">Buy Now</button></div>
					</div>
					<div style="font-size: 13px" class="mt-3"><strong>Ends In</strong></div>

					<div class="mt-3 d-inline-flex clockHolder align-items-center">

						<div class="d-flex align-items-center position-relative">
							<button class="btn btn-light  " id="days">
								3
							</button>

							<div class="position-absolute horizontallyCentered" style="bottom: -30px">DAYS</div>

						</div>

						<div>:</div>						

						<div class="d-flex align-items-center position-relative">
							<button class="btn btn-light  " id="days">
								33
							</button>

							<div class="position-absolute horizontallyCentered" style="bottom: -30px">HOURS</div>

						</div>

						<div>:</div>						

						<div class="d-flex align-items-center position-relative">
							<button class="btn btn-light  " id="mins">
								{{mins}}
							</button>

							<div class="position-absolute horizontallyCentered" style="bottom: -30px">MINS</div>

						</div>

						<div>:</div>						

						<div class="d-flex align-items-center position-relative">
							<button class="btn btn-light  " id="secs">
								{{secs}}
							</button>

							<div class="position-absolute horizontallyCentered" style="bottom: -30px">SECS</div>

						</div>


					</div>

				</div>
			</div>
			<div class="col-md-6 mt-5 mt-md-0">
				<div class="position-relative">
					<img src="/src/assets/images/featured.png" style="visibility: hidden;">
					
					<img style="position: absolute; top: 0; z-index: 2;" class="horizontallyCentered" src="/src/assets/images/featured.png">
					
					<div style="z-index: 0;background-color: rgb(221,237,235)" class="position-absolute rounded-circle fullyCentered popUpNdownAnimation "></div>
				</div>
			</div>
		</div>
	</div>
	
</div>

</template>

<style>
	

.clockHolder > div{
	margin-right: 10px;
	text-align: center;
}

.clockHolder button{
	    background: white;
    width: 70px;
    height: 70px;
    font-size: 30px;
    border-radius: 50%;
}



@media (max-width: 767px) {

	.featuredText{
		text-align: center;
	}

	.clockHolder button{
		width: 50px!important;
		height: 50px!important;
		font-size: 20px!important;
	}

}


@keyframes popUpNdown{
  0% {
    width: 300px;
    height: 300px;
  }
  50% {
    width: 400px;
    height: 400px;
  }
  100% {
    width: 300px;
    height: 300px;
  }
}

.popUpNdownAnimation{  

	animation: popUpNdown 2s infinite;
}

</style>