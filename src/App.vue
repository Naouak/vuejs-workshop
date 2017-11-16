<template>
    <div id="app">
        <ol class="list">
            <li v-for="(question, number) in questions">
                Question #{{number+1}} :
                <Question :question="question.question" :choices="question.choices"
                          :selected-choice="question.selectedChoice"
                          @answer-selected="(_, answer) => (question.selectedChoice = answer)"></Question>
            </li>
        </ol>

        <question-maker></question-maker>
    </div>
</template>

<script>
	import Question from './components/Question.vue';
	import QuestionMaker from './components/QuestionMaker.vue';

	export default {
		name: 'app',
		data() {
			return {
				questions: [
					{
						question: "Comment ça va ?",
						choices: ['Bien', 'Pas mal', 'Je suis malada', 'Comme un Lundi'],
						selectedChoice: null
					},
					{
						question: "Bien ou bien ?",
						choices: ['Bien', 'ou bien'],
						selectedChoice: null
					},
					{
						question: "Et la famille ?",
                        choices: ['Ça va, Ça va...', 'Imohtep'],
                        selectedChoice: null
					}
				]
			}
		},
		components: {
			Question,
            QuestionMaker
		}
	}
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        margin-top: 60px;
    }

    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: circle;
        padding: 0;
    }

    li {
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
