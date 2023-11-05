<script>
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
</script>

<div>
	<h2>Contact</h2>
	<div class="links">
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
</div>

<style>
	.links {
		display: flex;
		gap: 1rem;
	}

	a {
		color: var(--color-primary-100);
	}

	a:hover {
		color: var(--color-text);
	}
</style>
