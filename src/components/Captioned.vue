<script>
	
	
export default {
  mounted() {
    this.setFontSizeOfCaptionedElemnent('topCarouselShadow');
    window.addEventListener('resize', this.onWindowResize);
  },

  methods: {

    setFontSizeOfCaptionedElemnent() {
	     const captionImageWidth = document.getElementById('captionImage').offsetWidth

	      if(captionImageWidth > 400){
	        var captionHolders = document.getElementsByClassName('captionHolder');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.add('ml-5');
	          captionHolders[i].classList.add('mt-5');  
	        }
	        
	        var captionHolders = document.getElementsByClassName('captionHead');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.add('h2');
	      
	        }


	        var captionHolders = document.getElementsByClassName('captionRandom');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.add('h5')

	        }



	      }
	      else{
	        var captionHolders = document.getElementsByClassName('captionHolder');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.remove('ml-5');
	          captionHolders[i].classList.remove('mt-5'); 
	        }
	        
	        var captionHolders = document.getElementsByClassName('captionHead');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.remove('h2');
	      
	        }


	        var captionHolders = document.getElementsByClassName('captionRandom');
	        for(var i =0; i< captionHolders.length;i++){
	          captionHolders[i].classList.remove('h5')

	        }
	      }
    },
 
    onWindowResize() {
      this.setFontSizeOfCaptionedElemnent('topCarouselShadow');
    },

  },
  beforeDestroy() {
    window.removeEventListener('resize', this.onWindowResize);
  },
};






</script>


<template>
	<div id="captioned" class="mt-5">
	<div class="container">
		<div class="row">
			<div class="col-md-6">
				<div class="card captionCard position-relative" style="overflow: hidden;">

					<div class="line-animation"></div>

					<img class="card-img" id="captionImage" src="/src/assets/images/caption1.jpg" alt="Card image">
					<div class="card-img-overlay captionHolder w-50">
						
						<div class="card-title signatureColor captionRandom">
							Get 40% off
						</div>
						
						<div class="faded captionHead">
							Women's New Collection
						</div>
						
						<div class="mt-3 faded captionBadge">
							<i class="fa fa-angle-right"></i>
							<span style="margin-left: 5px;cursor: pointer;" ><strong>SHOP NOW</strong></span>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-6 captionCard mt-3 mt-md-0">
				<div class="card" style="overflow: hidden;">
					<div class="line-animation"></div>

					<img class="card-img" id="captionImage" src="/src/assets/images/caption2.jpg" alt="Card image">
					<div class="card-img-overlay captionHolder w-50">
						
						<div class="card-title signatureColor captionRandom">
							Stay Upto Date
						</div>
						
						<div class="faded captionHead">
							Men's Trendy Fashion
						</div>
						
						<div class="mt-3 faded captionBadge">
							<i class="fa fa-angle-right"></i>
							<span style="margin-left: 5px;cursor: pointer;" ><strong>SHOP NOW</strong></span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
</template>

<style>
	
.line-animation{
 position: absolute;
  width: 0;
  height:0;
  box-shadow: 0px -30px 30px -30px rgba(0, 0, 0, 0.6);
  top: 0px;
  display: none;
  left: 0px;
  transform: rotate(-45deg);
  animation: moveLine 1s forwards;
}

@keyframes moveLine {
  0% {
    width: 30%;
    height: 30%;
    left: 0;
    top: 0;
  }
  100% {
    width: 100%;
    height: 100%;
    left: calc(100% - 2px);
    top: calc(100% - 2px);
  }
}


.captionCard:hover .line-animation{
	display: block;
}



</style>