<script lang="ts">
	import './styles.css';
	import Header from '../components/Header.svelte';
	import Work from '../components/Work.svelte';
	import Notes from '../components/Notes.svelte';
	import Contact from '../components/Contact.svelte';
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

	<!-- Contact -->
	<section>
		<Contact />
	</section>
</main>

<style>
	main {
		margin: 4rem 0;
	}

	section {
		margin: 6rem 0;
	}
</style>
