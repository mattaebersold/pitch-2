<!-- Spacer block -->

<template lang='pug'>

section.max-w
	.cta
		.copy
			h2.style-h2 Let's Go
			p Sign up for a free account and start listing parts.
			btn-craft(:button='button')

		.image
			cloak-visual(
				noPlaceholder
				sizes='800px'
				image='imgs/cta.jpg'
				object-fit='cover')

</template>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<script lang='coffee'>
export default

	props: block: Object

	computed:

		button: ->
			return {
				label: 'Login or Signup'
				to: 'https://partstash.com'
			}

		# Root classes
		classes: -> "height-#{@block.height}"

</script>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<style lang='stylus' scoped>

.cta
	background #303030
	border-radius 20px
	display flex
	align-items center
	overflow hidden
	
.image, .copy
	width 50%

.copy
	padding 0 40px

@media(max-width:768px)
	.cta
		flex-wrap wrap

	.image
		height 300px
		order 1
		overflow hidden

	.copy
		order 2
		padding 40px

	.image, .copy
		width 100%

</style>
