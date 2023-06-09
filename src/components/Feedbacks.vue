<script setup>
	
	import Feedback from './Feedback.vue'

</script>

<script>
	export default{
		data(){
			return{
				feedbacks: [
					{
						text: 'Bobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco laborisBobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco laborisBobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco',

						author: 'KP Oli',
						
						authorJob: 'Scientist'
					
					},

					{
						text: 'Bobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco laborisBobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco laborisBobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco',

						author: 'Donald Trump',
						
						authorJob: 'Web Developer'
					
					},


				]
			}
		}
	};
</script>


<template>
	
	<div id="feedback" class="position-relative mt-5" style="overflow:hidden; background-color: rgb(247,248,251)">

		<div class=" d-none d-md-block shadow rounded-circle position-absolute" style="bottom:-180px; left:200px; width: 300px;height: 300px;background-color: rgb(223,237,236) "></div>

		<div class="shadow d-none d-md-block rounded-circle position-absolute" style="top:-100px; right:-300px; width: 600px;height: 600px;background-color: rgb(223,237,236) "></div>


		<div class="container pt-5 pb-5">
			<div class="row pt-5">
				<div class="col-md-4">
					<div style="width: 80%">
						<div class="h3">
							What Customers Say About Us
						</div>
						<p class="faded">
							Bobore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitat ion ullamco laboris
						</p>

						<div class="mt-4 mb-4 mb-md-0">
						    <button  href="#feedbacksHolder" role="button" data-slide="prev" class="btn btn-light controlIcon" aria-hidden="true">
						    	<i class="fa fa-angle-left"></i>
						    </button>
						    <button  href="#feedbacksHolder" role="button" data-slide="next" class="btn btn-light controlIcon" aria-hidden="true">
						    	<i class="fa fa-angle-right"></i>
						    </button>
						</div>
					</div>
				</div>
				
				<div class="col-md-8  carousel slide" id="feedbacksHolder">

					<div class="carousel-inner" style="padding-bottom:80px">
						
						<ol class="carousel-indicators">
					      <li data-target="#feedbacksHolder" data-slide-to="0" class="active"></li>
					      <li data-target="#feedbacksHolder" data-slide-to="1"></li>
					      <li data-target="#feedbacksHolder" data-slide-to="2"></li>
					    </ol>

					    <div class="carousel-item active">
							<div class="row">
								<Feedback v-for="feedback in feedbacks" :feedback="feedback" />
							</div>
						</div>

						<div v-for = "index in 2" class="carousel-item">
							<div class="row">
								<Feedback v-for = "feedback in feedbacks" :feedback = "feedback" />	
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>

</template>