<template>
	<div>
		<li v-for="todo in todos" v-bind:key="todo.text">This is a todo: {{todo.text}}</li>
	</div>
</template>

<script>
	export default {
		name: 'TodoItem',
		props: ['todos']
	};
</script>