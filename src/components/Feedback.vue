<script>

export default{

	props: {
		feedback: Object
	}

};	

</script>


<template>
	
	<div class="col-md-6">
		<div class="card feedback  p-4">
			<div class="d-flex align-items-center justify-content-between mt-3">
				<div>
					<i class="signatureColor fa fa-quote-left fa-3x"></i>
				</div>
				<div style="font-size: 20px">
					<span v-for = "index in 5" >&#9733;</span>
				</div>
			</div>
			<div class=" mt-3 faded" style="font-style: italic;">
				{{feedback.text}}
			</div>
			<div class="mt-4 mb-2 d-flex">
				<div>
					<img class="rounded-circle" src="/src/assets/category/person1.jpg">
				</div>
				<div style="margin-left: 25px">
					<div style="margin-bottom: 5px" class="h5">
						{{feedback.author}}
					</div>
					<span class="faded">{{feedback.authorJob}}</span>
				</div>
			</div>

		</div>		
	</div>

</template>


<style>

.feedbackHolder{
	background: white;
}

.feedback{
	border: none;
}

</style>