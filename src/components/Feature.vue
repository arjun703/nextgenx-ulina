<script>
export default {
  props: {
    icon: String, heading: String, text: String
  }
};
</script>


<template>
	<div class="col-lg-3 col-md-4 col-sm-6">
		<div class="d-flex">
			<div class="signatureColor">
				<i :class="'fa ' + icon + ' fa-3x'"></i>				
			</div>
			<div class="featureDesc ml-3">
				<h4>{{ heading }}</h4>
				<p>{{ text }}</p>
			</div>
		</div>
	</div>
</template>