<script setup>
	import Feature from './Feature.vue';
</script>


<template>
	<div class="container mt-5">
	  <div class="row">
	    
	    <Feature :icon = " 'fa-truck' " 
	    		 :heading= " 'Free Shipping' " 
	    		 :text=" 'lorem imds dsf sfdsf dsfdsf sdfsdfk sdf sdf sdf' " 
	   	/>
	    
	    <Feature :icon = " 'fa-credit-card' " 
	    		 :heading= " 'Secure Payments' " 
	    		 :text=" 'lorem imds dsf sfdsf dsfdsf sdfsdfk sdf sdf sdf' " 
	   	/>
	    
	    <Feature :icon = " 'fa-arrows-rotate' " 
	    		 :heading= " 'Easy Returns' " 
	    		 :text=" 'lorem imds dsf sfdsf dsfdsf sdfsdfk sdf sdf sdf' " 
	   	/>     

	   	<Feature :icon = " 'fa-solid fa-clock' " 
	    		 :heading= " '24 / 7 Support' " 
	    		 :text=" 'lorem imds dsf sfdsf dsfdsf sdfsdfk sdf sdf sdf' " 
	   	/>

	  </div>
	</div>
</template>