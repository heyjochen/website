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
	<h2>Notes</h2>
	<p>
		I invest a significant portion of my time in staying updated on the latest trends in Software
		Engineering, and have developed a workflow to summarize articles and posts. I'm excited to share
		some of my favorite findings with you:
	</p>
	<ul>
		{#each notes as note}
			<li>
				<a href={note.href} target="_blank">
					<span class="title">{note.title}</span>
					<!-- <p>{note.desc}</p> -->
					<span class="tags">#{note.tags}</span>
				</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	ul {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		margin-top: 1rem;
	}
	li {
		padding: 0;
		list-style: none;
	}

	a {
		background-color: var(--color-primary-700);
		display: flex;
		gap: 0.25rem;
		flex-direction: column;
		cursor: pointer;
		padding: 1rem;
		border: 1px solid var(--color-primary-600);
		text-decoration: none;
		border-radius: var(--border-radius);
		color: var(--color-text-1);
	}

	a:hover {
		border: 1px solid var(--color-primary-600);
	}

	.title {
		text-overflow: ellipsis;
		overflow-x: hidden;
		white-space: nowrap;
		color: var(--color-text);
		font-weight: bold;
	}

	.tags {
		color: var(--color-primary-200);
	}
</style>
