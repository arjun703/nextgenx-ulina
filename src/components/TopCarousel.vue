<script setup>
	import CarouselItem from './CarouselItem.vue'
	import LeftRightButton from './buttons/LeftRight.vue'
</script>


<script>
	
export default {
  mounted() {
    this.setShadowHeight('topCarouselShadow');
    window.addEventListener('resize', this.onWindowResize);
  },

  methods: {

    setShadowHeight(classs) {
	    const elements = document.querySelectorAll(`.${classs}`);
	    var parentWidth;
	    // Iterate over the elements
	    for (let i = 0; i < elements.length; i++) {
	        const div = elements[i];
	      // Do something with each element
	        parentWidth = div.parentNode.clientWidth;
	      if(parentWidth != 0){
	        break;
	      } 
	     
	    }


	    // Iterate over the elements
	    for (let i = 0; i < elements.length; i++) {
		    const div = elements[i];
		    const width = parentWidth * 0.85;
		    div.style.width = `${width}px`
		    div.style.height = `${width}px`
	     
	    }

    },
 
    onWindowResize() {
      this.setShadowHeight('topCarouselShadow');
    },

  },
  beforeDestroy() {
    window.removeEventListener('resize', this.onWindowResize);
  },
};


</script>


<template>
	
	<div id="carouselExampleIndicators" class="carousel slide " style="background-color: var(--bgColor)" data-ride="carousel">
		
		<div class="carousel-inner">

		    <ol class="carousel-indicators">
		   
		      <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
		      <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
		      <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
		   
		    </ol>
	    

	  
		   <CarouselItem  :active = "true"   :imgSrc = " 'mantop.png' " />
		   <CarouselItem  :active = "false"  :imgSrc = " 'girltop.png' " />
		   <CarouselItem  :active = "false"  :imgSrc = " 'mantop2.png' " />


		  <LeftRightButton 
		  				:purpose = " 'carousel-control-prev' "
		  				:role = " 'prev' "
		  				:icon = " ' fa-angle-left ' " 
		  				:href = " '#carouselExampleIndicators' "
		  />

		  <LeftRightButton 
		  				:purpose = " 'carousel-control-next' "
		  				:role = " 'next' "
		  				:icon = " ' fa-angle-right ' " 
		  				:href = " '#carouselExampleIndicators' "
		  />

		</div>
	
	</div>

</template>

<style>



  .carousel-indicators {
    bottom: 5px;
    left: 0;
    right: 0;
    text-align: center;

  }
  
  .carousel-indicators li {
    display: inline-block;
    width: 8px;
    height: 8px;
    opacity: 0.6;
    border-radius: 50%;
    background-color: black;
    cursor: pointer;
    padding: 8px;
  }
  
  .carousel-indicators .active {
	background-color: red;  	
	opacity: 1;
  }

  @keyframes popup{
	from{
		scale:0;
	}
	to{
		scale:1;
	}
}

.popupAnimation{
	animation: popup 2s;
}

</style>