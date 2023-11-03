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
					<div class="title-container">
						<span class="title">{note.title}</span>
						<!-- <p>{note.desc}</p> -->
						<span class="tags">#{note.tags}</span>
					</div>
					<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
						><path
							fill="currentColor"
							d="M5.615 20q-.69 0-1.152-.462Q4 19.075 4 18.385V5.615q0-.69.463-1.152Q4.925 4 5.615 4h5.616v1H5.615q-.23 0-.423.192Q5 5.385 5 5.615v12.77q0 .23.192.423q.193.192.423.192h12.77q.23 0 .423-.192q.192-.193.192-.423v-5.616h1v5.616q0 .69-.462 1.152q-.463.463-1.153.463H5.615Zm4.123-5.03l-.707-.708L18.292 5H14V4h6v6h-1V5.708l-9.262 9.261Z"
						/></svg
					>
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
		justify-content: space-between;
		align-items: center;
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

	.title-container {
		display: flex;
		gap: 0.25rem;
		flex-direction: column;
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
