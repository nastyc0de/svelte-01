<script>
	import About from "./components/About.svelte";
	import Person from "./components/Person.svelte";
	import Skills from "./components/Skills.svelte";
	import Text from "./components/Text.svelte";
	export let name;
	export let lastName;

	const data = {
		name: 'Ben',
		lastName: '10',
		age:100
	}
</script>

<main>
	<h1>Hello {name} {lastName}!</h1>
	<About/>
	<Text anotherText='Hola Comunidad'/>
	<Person {...data}/>
	<Skills/>
	
</main>

<style>
	:global(body){
		background-color: bisque;
	}
	:global(:root){
		--color-p:#066e6e;
	}
	:global(body.dark-mode){
		background-color: #1c1f1c;
		color:blanchedalmond
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>