<template lang="pug">
section
	.title
		h1 Pricing
	.container
		.header
			p  With design packages starting at just £199, our services can be tailored to suit every budget.
		.main
			.starting
				span Starting  From 
				br             
				span.value £199
				br
				span.subtext Per Roon Excl. VAT
			.footerSteps
				p VISUAL MOODBOARD
				p DESIGN PRESNTATION
				p CURATED SHOPPING LIST 
	.title
		h2 Extra  
	.content
		.header
			p As part of our hassle-free philosophy, we offer personalised services designed to cater to your needs and more.
		.main
			ul
				price-card.price(v-for="(p, i) in data", :key="i", :price="p") 
	.title
		h2 Bespoke
	.summary
		.head
			p Get in touch with us for Bespoke services.
		.btn.btn-primary
			a SCHEDULE A CALL WITH OUR DSIGNER


</template>
<script>
import PriceCard from './PriceCard';

export default {
	components: {
		PriceCard
	},
	data (){
		return{
			data:[
				{name: "SITE VISIT", value: '£100'},
				{name: "BUYING MANAGEMENT", value: '£35 p/h'},
				{name: "INSTALLATION", value: ' £50 p/h'},
				{name: "DELIVERY MANAGEMENT AND STORAGE", value: '£80 p/h'},
				{name: "STYLING", value: ' £50 p/h'}
			]
		}

	}
		
}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
section
	// margin: 3rem 3rem 1rem 3rem
	padding: 5rem 2rem 2rem 3rem
	font-family: futura-pt,sans-serif
	.container
		opacity: .9
		font-size: 2rem
		display: flex	
		margin-bottom: 3rem
		font-weight: 100
		@media(max-width: 1000px)
			display: block
		.header
			margin-right: 9%
			width: 35%
			flex: 4
			@media(max-width: 1000px)
				width: 100%
				margin-bottom: 2rem
		.main
			display: flex
			flex: 7
			@media(max-width: 1000px)
				display: block
			.starting
				margin-right: 9%
				.value
					font-size: 2.5rem
					font-weight: 500
				.subtext
					font-weight: 300
					font-size: .7rem
			.footerSteps
				p
					font-size: 1.2rem
					font-weight: 300
					line-height: 3rem
					text-transform: uppercase
section
	.content
		font-size: 2rem
		display: flex
		@media(max-width: 1000px)
			display: block
		.header
			flex: 4
			font-weight: 100
			margin-right: 10%
			margin-bottom: 4rem
		.main
			flex: 7
			ul
				@include reset
				@include flex
				justify-content: flex-start
				flex-wrap: wrap
			
				.price
					width: 12rem
					margin-right: 1rem
					margin-bottom: 3rem
section
	.summary	
		display: flex
		font-size: 2rem
		font-weight: 100
		opacity: .9
		@media(max-width: 1000px)
			display: block
		.head
			flex: 4
			margin-bottom: 2rem
		.btn.btn-primary
			flex: 6
			text-align: center
			color: #FFF
			
			@media(max-width: 1000px)
				width: 50%
			a
			
</style>
