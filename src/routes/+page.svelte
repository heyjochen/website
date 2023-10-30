<script lang="ts">
	import './styles.css';
	import Header from '../components/Header.svelte';
	import Work from '../components/Work.svelte';
	import Notes from '../components/Notes.svelte';
</script>

<svelte:head>
	<title>Jochen Stierberger</title>
	<meta name="description" content="Jochen Stierberger's Website" />
</svelte:head>

<main>
	<Header />
	<!-- Work -->
	<section>
		<Work />
	</section>

	<!-- Notes -->
	<section>
		<Notes />
	</section>
</main>

<style>
	main {
		margin-top: 8rem;
	}
</style>
