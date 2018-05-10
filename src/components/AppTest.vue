<template>
	<div>
	
		<!-- <slot name="header"></slot>
		<slot name="footer"></slot> -->
		<slot :color = "color" :lastName = "lastName"></slot>
	</div>
</template>

<script>
	
	export default {

		data() {
			return {
				color: 'Blue',
				lastName: 'blabla'
			}
		}


	}	
</script>

