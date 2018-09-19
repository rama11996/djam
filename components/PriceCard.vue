<template lang="pug">
li.price
	span.name {{ price.name }}
	span.value {{ price.value }}
</template>

<script>
export default {
    props: ['price']
}
</script>


<style lang="sass" scoped>
.price
	.value
		font-size: 2.5rem
		line-height: 3.5rem
		font-weight: 500
	.name
		opacity: .8
		font-size: 12px
		font-weight: 500
		line-height: 16px
		text-transform: uppercase
		display: block
		height: 2rem
	
    
</style>
