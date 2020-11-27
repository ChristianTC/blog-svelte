<script>
	import Nav from '../components/Nav.svelte';
	import Main from '../components/Main.svelte';
	import Header from '../components/Header.svelte';

	export let segment;
</script>
<Header />

<Nav {segment}/>

<Main>
	<slot></slot>
</Main>