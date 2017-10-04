<template>
  <div class="question">
    <h2>{{question}}</h2>

    <ul>
      <li v-for="choice in choices">
        <choice :text="choice"></choice>
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
      }
    },
		data() {
			return {}
		},
		methods: {},
		components: {
			Choice
    }
	}
</script>
