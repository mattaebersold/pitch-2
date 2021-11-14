<!-- Simple text over a white background -->

<template lang='pug'>

section.hero-marquee.max-w-full(:style='styles')

	.content.max-w

		cloak-visual.logo(
			sizes='300px'
			:image='block.logo')

		//- Optional list of buttons
		.buttons(v-if='hasButtons'): btn-craft(
			v-for='button in block.buttons' :key='button.id'
			:button='button')

</template>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<script lang='coffee'>
export default

	props: block: Object

	computed: 

		hasButtons: -> @block.buttons?

		styles: ->
			backgroundImage: "url(#{@block.image}"
			

</script>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<style lang='stylus' scoped>

.hero-marquee

	min-height 500px
	display flex
	align-items center
	justify-content center
	background-size cover
	background-position center center

	// Put text on a dark background
	// background lighten(primary-color, 10%)
	color white

	// Make it look centered _after_ the header
	&:before
		content ''
		display block
		+tablet-up()
			height header-h
		+tablet-down()
			height mobile-header-h

	// Add internal spacing
	fluid-space padding-v, 'l'

	// Center text
	text-align center

// Optional buttons
.buttons

	.btn
		margin-h 10px

	// Push away from copy
	&:not(:first-child)
		fluid-space margin-top, 's'


.logo
	width 200px
	margin 0 auto


</style>
