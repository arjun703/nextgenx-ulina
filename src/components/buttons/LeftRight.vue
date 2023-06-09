<script>
export default {
  props: {
    icon: String, purpose:String, role: String, href: String
  }
};
</script>


<template>
	<a :class=" purpose  + ' d-none d-md-flex ' " :href="href" :data-slide="role">
		<button class="btn btn-light fs-18 rounded-circle border border-secondary" aria-hidden="true">
			<i :class="'fa ' + icon"></i>
		</button>
		<span class="sr-only">{{ role }}</span>
	</a>
</template>

<style scoped>
	
</style>