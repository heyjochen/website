<script lang="ts">
	const notes = [
		{
			title: 'On Writing well',
			tags: ['book'],
			href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-01-books/on-writing-well/'
		},
		{
			title: 'How to become a better Software Engineer',
			tags: ['blog'],
			href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/how-to-become-a-better-software-engineer/'
		},
		{
			title: 'Large Technical Projects',
			tags: ['blog'],
			href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/large-technical-projects/'
		},
		{
			title: 'Culture of Excellence',
			tags: ['blog'],
			href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/culture-of-excellence/'
		}
	];
</script>

<div>
	<h4>Notes</h4>
	<ul>
		{#each notes as note}
			<li>
				<a href={note.href} target="_blank">
					<span class="title">{note.title}</span>
					<!-- <p>{note.desc}</p> -->
					<span>#{note.tags}</span>
				</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	ul {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 1rem;
		margin-top: 1rem;
	}
	li {
		padding: 0;
		list-style: none;
	}

	a {
		display: flex;
		gap: 0.25rem;
		flex-direction: column;
		cursor: pointer;
		padding: 1rem;
		border: 1px solid var(--color-primary);
		text-decoration: none;
		border-radius: 1rem;
		color: var(--color-text-1);
	}

	a:hover {
		border: 1px solid var(--color-secondary);
	}

	.title {
		text-overflow: ellipsis;
		overflow-x: hidden;
		white-space: nowrap;
		width: 12rem;
		color: var(--color-text-0);
	}
</style>
