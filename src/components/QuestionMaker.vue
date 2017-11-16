<template>
    <form>
        <label>Question : <input type="text" v-model="questionText"></label>

        <fieldset>
            <question :question="questionText" :choices="[]"></question>
        </fieldset>
    </form>
</template>

<script>
    import Question from './Question.vue';

	export default {
		data(){
			return {
				questionText: ''
            }
        },
		name: "question-maker",
        components: {
			Question
        }
	}
</script>

<style scoped>

</style>