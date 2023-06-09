<script>
export default {
  props: {
	active: Boolean, imgSrc: String 
 },
 data() {
    return {
      img: '/src/assets/images/'+this.imgSrc
    };
  }
};
</script>

<template>

	<div :class="['carousel-item', { active }]">
    	
    	<div class="container">
    		
    		<div class="row">
    			
    			<div class="col-md-6 d-flex align-items-center">
					<div class="topCarouselText">
						<div class="topCarouselSale " style="color: var(--topCarouselColor)">
							SUMMER SALE IS ON
    					</div>
    					<div class="topCarouselHeading">
    						<h1 style="opacity: 0.8">
    							Discover Men's Latest Fashion
    						</h1>
    					</div>
    					
    					<div class="topCarouselButton">
    						<button  class="btn mt-2 exploreBtn buttonMyOwn roundedButton">
    							Explore Now
    						</button>
    					</div>
					</div>
    			</div>
    			
    			<div class="col-md-6" style="position: relative;" >
    				
    				<div style="height: 100vh"></div>
    				
    				<img class="popupAnimation w-100 position-absolute" 
    					:src="img" style="top: 0; z-index:20;">
    				
					<div class="topCarouselShadow rounded-circle horizontallyCentered position-absolute w-80" 
    					 style="background: white; top: 50px; z-index: 0;"></div>
    		
    			</div>
    		
    		</div>
    	
    	</div>
    
    </div>

</template>

<style>

.buttonMyOwn{
	background-color: var(--topCarouselColor);
	color: white;
}

.roundedButton{
	border-radius: 20px;
}
	
@media (max-width: 2000px) {

	.topCarouselText{
		margin-left: 15%;
	}

}

@media (max-width: 767px) {
	
	.topCarouselText{
		text-align: center;
		margin-left: 0;
		height: auto;

	}

	.topCarouselSale{
		font-size: 18px;
		font-weight: bold;
		margin-top: 100px;
	}

	.topCarouselHeading{
		margin-top: 50px;
		margin-bottom: 50px;
	}

	.exploreBtn{
		margin-bottom: 40px;
		padding: 15px 40px 15px 40px;
		border-radius: 120px;
	}

	.featuredText{
		text-align: center;
	}

	.clockHolder button{
		width: 50px!important;
		height: 50px!important;
		font-size: 20px!important;
	}
}

</style>