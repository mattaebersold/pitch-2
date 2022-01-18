<!-- Layout footer -->

<template lang='pug'>

footer.layout-footer: .max-w 
	p Copyright 2022 Partstash. 
	a(href='mailto:support@partstash.com') Contact Support

</template>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<script lang='coffee'>
# export default
# 	components:
# 	props: []
# 	data: ->
# 	computed:
# 	watch:
# 	methods:
</script>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<style lang='stylus' scoped>

.layout-footer
	background #090909
	fluid-space padding-v, 'm'

a
	font-style italic
	font-weight bold

</style>
