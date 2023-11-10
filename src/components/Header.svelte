<script lang="ts">
	// const nav = [
	// 	{
	// 		name: 'Home',
	// 		link: '/'
	// 	},
	// 	{ name: 'Notes', link: 'https://notes.stierberger.com' }
	// ];
</script>

<header>
	<!-- <nav> -->
	<!-- 	<ul> -->
	<!-- 		{#each nav as entry} -->
	<!-- 			<li> -->
	<!-- 				<a href={entry.link} target="_blank"> -->
	<!-- 					{entry.name} -->
	<!-- 				</a> -->
	<!-- 			</li> -->
	<!-- 		{/each} -->
	<!-- 	</ul> -->
	<!-- </nav> -->
	<h1>hey, I'm Jochen.</h1>
	<!-- FIX: this change position -->
	<p>
		I'm a Software Developer at nvisia, where I build cutting-edge IoT applications.<br />
		I deeply care about the quality & performance of the products shipped and take a thoughtful, practical
		approach to problem-solving that considers tradeoffs and avoids over-engineering<br />
	</p>
	<p>
		I had the privilege of working on three different continents.<br /> I love pizza, tinkering with
		recipes and shooting large-format photographs on film.
	</p>
</header>

<style>
	header {
		margin-top: 6rem;
	}

	/* ul { */
	/* 	display: flex; */
	/* 	justify-content: flex-end; */
	/* 	gap: 0.75rem; */
	/* 	margin-bottom: 4rem; */
	/* } */
	/**/
	/* li { */
	/* 	list-style-type: none; */
	/* } */
	/**/
	/* a { */
	/* 	color: var(--color-primary-100); */
	/* } */
	/**/
	/* a:hover { */
	/* 	color: var(--color-text); */
	/* } */

	h1 {
		font-size: 1.5rem;
		font-weight: 600;
	}

	h1::before {
		content: '';
		position: absolute;
		top: -25px;
		left: 0;
		right: 0;
		width: 100%;
		height: 800px;
		background-position: top;
		background-size: cover;
		/* background-image: radial-gradient( */
		/* 	78.57% 78.57% at 55.65% 0.84%, */
		/* 	#a0aaba 0, */
		/* 	#4d586a 0, */
		/* 	rgba(15, 23, 42, 0) 100% */
		/* ); */
		opacity: 0.1;
		z-index: -1;
		border-radius: inherit;
		filter: blur(110px);
	}

	p {
		max-width: 40rem;
	}
</style>
