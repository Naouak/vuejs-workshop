<template>
    <div @click="choiceSelected" :style="{ 'font-weight': this.selected?'bold':'normal'}">
        {{text}}
    </div>
</template>
<style>
</style>
<script>
	export default {
		props: {
			text: {
				required: true
			},
            selected: {
				default: false
            }
		},
		data() {
			return {}
		},
		methods: {
			choiceSelected() {
				this.$emit('choice-selected', this.text);
			}
		},
		components: {}
	}
</script>
