<template>
    <div class="question">
        <h2>{{question}}</h2>

        <ul>
            <li v-for="choice in choices">
                <choice :text="choice" :selected="choice===selectedChoice" @choice-selected="choiceSelected"></choice>
            </li>
        </ul>

        <hr>
    </div>
</template>
<style>
</style>
<script>
	import Choice from './Choice.vue';

	export default {
		props: {
			question: {
				required: true
			},
			choices: {
				required: true
			},
            selectedChoice: {
				default: null
            }
		},
		data() {
			return {}
		},
		methods: {
			choiceSelected(choice) {
				this.$emit('answer-selected', this.question, choice);
			}
		},
		components: {
			Choice
		}
	}
</script>
