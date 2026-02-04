<script>
	import About from "./components/About.svelte";
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte";
	import Skills from "./components/Skills.svelte";
	import Input from "./components/Input.svelte";
	import Photos from "./components/Photos.svelte";
	export let name;
	export let lastname;

	const data = {
		name: "Svelte",
		lastname: "Framework",
		age: 31
	};
</script>
<style>
	:global(body){
		background-color: #f2eee2;
		color: #0084f6;
	}
	:global(:root){
		--theme-color: purple;
	}

	:global(body.dark-mode){
		background-color: #1d3040;
		color: #bfc2c7;
	}
</style>

<main>
	<h1>Hello {name} {lastname}!</h1>
	<About />
	<Text anotherText="Hola Jose Luis" />
	<Text />
	<Person  {...data} />
	<Skills />
	<Input />
	<Photos />
</main>