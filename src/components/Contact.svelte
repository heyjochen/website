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
			<a href={link.href} target="_blank">{link.name}</a>
		{/each}
	</div>
</div>

<style>
	.links {
		display: flex;
		gap: 1rem;
	}
</style>
