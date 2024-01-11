<script lang="ts">
	let notes = {
		Books: {
			active: true,
			entries: [
				{
					title: 'On Writing well',
					tags: ['improvement'],
					href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-01-books/on-writing-well/'
				},
				{
					title: "So good they can't ignore you",
					tags: ['improvement'],
					href: 'https://notes.stierberger.com/10-19-personal/10-personal-development/10-01-books/so-good-they-can-t-ignore-you/'
				},
				{
					title: 'Deep Work',
					tags: ['improvement'],
					href: 'https://notes.stierberger.com/10-19-personal/10-personal-development/10-01-books/deep-work/'
				},
			]
		},
		Blogs: {
			active: false,
			entries: [
				{
					title: 'How to become a better Software Engineer',
					tags: ['improvement'],
					href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/how-to-become-a-better-software-engineer/'
				},
				{
					title: 'Large Technical Projects',
					tags: ['best_practices'],
					href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/large-technical-projects/'
				},
				{
					title: 'Culture of Excellence',
					tags: ['best_practices'],
					href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/culture-of-excellence/'
				},
				{
					title: 'How to do great Code Reviews?',
					tags: ['improvement'],
					href: 'https://notes.stierberger.com/20-29-software-engineering/20-personal-development/20-02-blogs/how-to-do-great-code-reviews/'
				}
			]
		}
	};

	function switchTab(tabKey: string) {
		const updatedNotes = { ...notes };

		// Check if the clicked tab is already active
		const isTabActive = updatedNotes[tabKey as keyof typeof notes].active;

		// Update the active property for the clicked tab only if it's not already active
		if (!isTabActive) {
			updatedNotes[tabKey as keyof typeof notes] = {
				...updatedNotes[tabKey as keyof typeof notes],
				active: true
			};
		}

		// Set active property to false for all other tabs
		Object.keys(updatedNotes).forEach((otherTabKey) => {
			if (otherTabKey !== tabKey) {
				updatedNotes[otherTabKey as keyof typeof notes] = {
					...updatedNotes[otherTabKey as keyof typeof notes],
					active: false
				};
			}
		});

		notes = updatedNotes;
	}
</script>

<div>
	<h2>Notes</h2>
	<p class="intro">
		I invest a significant portion of my time in staying updated on the latest trends in Software
		Engineering, and have developed a workflow to summarize articles and posts. I'm excited to share
		some of my favorites with you:
	</p>
	<section>
		{#each Object.entries(notes) as [key, value]}
			<button class={value.active ? 'active' : ''} on:click={() => switchTab(key)}>
				{key}
			</button>
		{/each}
		<ul>
			{#each Object.entries(notes) as [_, value]}
				{#if value.active}
					{#each value.entries as note}
						<li>
							<a href={note.href} target="_blank">
								<div class="title-container">
									<span class="title">{note.title}</span>
									<!-- <p>{note.desc}</p> -->
									<span class="tags">#{note.tags}</span>
								</div>
								<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
									><path
										fill="#a4a4a2"
										d="M14 3v2h3.59l-9.83 9.83l1.41 1.41L19 6.41V10h2V3m-2 16H5V5h7V3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7h-2v7Z"
									/></svg
								>
							</a>
						</li>
					{/each}
				{/if}
			{/each}
		</ul>
	</section>
</div>

<style>
	.intro {
		max-width: 40rem;
	}

	button {
		font-size: 1rem;
		background: transparent;
		color: var(--color-primary-100);
		border: none;
		margin-right: 1rem;
		cursor: pointer;
		padding: 0;
	}

	button:hover {
		text-decoration: underline;
	}

	button.active {
		color: var(--color-primary);
		text-decoration: underline;
	}

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
		border: 1px solid var(--color-border);
		text-decoration: none;
		border-radius: var(--border-radius);
		color: var(--color-text-1);
	}

	a:hover {
		border: 1px solid var(--color-border-100);
		filter: brightness(1.1);
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

	@media (max-width: 480px) {
		.title {
			max-width: 17rem;
		}
	}
</style>
