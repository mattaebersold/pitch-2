<!-- Desktop header -->

<template lang='pug'>

detachable-header.layout-header-desktop(:height='height')
	header.max-w-full: .columns.max-w-medium
		.left
			nuxt-link(to='/') Partstash

		.right
			smart-link(to='/features') Features
			smart-link(to='/about') About
			smart-link(to='/faq') FAQ
			smart-link(to='https://partstash.com') Login/Register

</template>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<script lang='coffee'>
import DetachableHeader from 'vue-detachable-header'
import 'vue-detachable-header/index.css'
import dimensions from '~/assets/vars/dimensions'
export default

	components: { DetachableHeader }

	data: -> height: parseInt dimensions['header-h']

</script>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<style src='./header.styl' lang='stylus' scoped></style>
<style lang='stylus' scoped>

.layout-header-desktop
	+tablet-down()
		display none

	>>> a
		display inline-block
		font-weight bold
		margin 0 10px

</style>
