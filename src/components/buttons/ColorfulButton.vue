<script>
export default {
  props: {
  	icon: String
  }
};
</script>


<template>
	
	<div>
		<button  class="btn btn-light colorfulButton  rounded-circle shadow-sm">	
			<i :class=" 'fa '+ icon "></i>
		</button>			    			
	</div>

</template>

<style>
	.colorfulButton{
		background:white; 
		width: 46px; 
		height: 46px; 
		margin-left: 8px;
		font-size: 18px;  									
		color:var(--topCarouselColor);
		transition: 0.5s ease;
		box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
	}
	.colorfulButton:hover{
		background: var(--topCarouselColor);
		color: white;
	}
</style>