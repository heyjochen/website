<script lang="ts">
	const links = [
		{
			name: 'Email',
			title: 'Email',
			href: 'jochen@stierberger.com'
		},
		{
			name: 'LinkedIn',
			title: '@jochenstierberger',
			href: 'https://www.linkedin.com/in/jochenstierberger/'
		},
		{
			name: 'GitHub',
			title: '@heyjochen',
			href: 'https://github.com/heyjochen'
		}
	];

	function showWidget() {
		Calendly.initPopupWidget({ url: 'https://calendly.com/heyjochen/meet' });
	}
</script>

<div>
	<h2>Contact</h2>
	<div class="links">
		<div class="left">
			{#each links as link}
				{#if link.name !== 'Email'}
					<a href={link.href} target="_blank">
						{link.name}
					</a>
				{:else}
					<a href="mailto:jochen@stierberger.com" target="_blank">
						{link.name}
					</a>
				{/if}
			{/each}
		</div>
		<!-- Calendly link widget begin -->
		<button class="calendly" on:click={showWidget}>
			<svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 256 256"
				><path
					fill="currentColor"
					d="M208 32h-24v-8a8 8 0 0 0-16 0v8H88v-8a8 8 0 0 0-16 0v8H48a16 16 0 0 0-16 16v160a16 16 0 0 0 16 16h160a16 16 0 0 0 16-16V48a16 16 0 0 0-16-16Zm-96 152a8 8 0 0 1-16 0v-51.06l-4.42 2.22a8 8 0 0 1-7.16-14.32l16-8A8 8 0 0 1 112 120Zm56-8a8 8 0 0 1 0 16h-32a8 8 0 0 1-6.4-12.8l28.78-38.37a8 8 0 1 0-13.31-8.83a8 8 0 1 1-13.85-8A24 24 0 0 1 176 136a23.76 23.76 0 0 1-4.84 14.45L152 176ZM48 80V48h24v8a8 8 0 0 0 16 0v-8h80v8a8 8 0 0 0 16 0v-8h24v32Z"
				/></svg
			>
		</button>
	</div>
</div>

<style>
	.links {
		display: flex;
		justify-content: space-between;
	}

	.left {
		display: flex;
		align-items: center;
		gap: 1rem;
	}

	a {
		color: var(--color-primary-100);
	}

	a:hover {
		color: var(--color-primary);
	}

	.calendly {
		background: transparent;
		border: none;
		padding-right: 0.6rem;
	}

	svg {
		color: var(--color-primary-100);
		cursor: pointer;
	}

	svg:hover {
		color: var(--color-primary);
	}
</style>
