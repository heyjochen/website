<script lang="ts">
	const work = [
		{
			name: 'nvisia',
			location: 'Chicago, IL',
			position: [
				{
					name: 'Software Engineer',
					start: 'Nov 2023',
					end: 'present',
					task: [
						'My team develops an IoT platform that integrates 24/7 monitoring and real-time alerts, empowering our customers to optimize their operational uptime.',
						'I have expertise in TypeScript/JavaScript and can navigate different languages and technology stacks.'
					]
				},
				{
					name: 'Software Developer',
					start: 'Oct 2022',
					end: 'Nov 2023',
					task: [
						'I designed and implemented an internal tool that automated a tedious manual process, enhancing the developer experience and delivering cost and effort savings.',
						'I refactored components, removed lines of code, and fine-tuned data fetching for efficiency.'
					]
				}
			]
		},
		{
			name: '100Devs',
			location: 'Remote',
			position: [
				{
					name: 'Software Engineer',
					start: 'Jan 2022',
					end: 'Oct 2022',
					task: [
						'I developed applications for small local businesses, collaborated with designers and offered valuable tradeoff suggestions to business stakeholders when necessary.'
					]
				}
			]
		},
		{
			name: 'The Field Museum',
			location: 'Chicago, IL',
			position: [
				{
					name: 'Studio Manager',
					start: 'Jun 2021',
					end: 'Jan 2022',
					task: [
						'I created high-magnification photographs and 3D models, enhanced fossil preparation as well as specimen research and developed marketing assets across various media channels.'
					]
				}
			]
		}
	];
</script>

<div>
	<h2>Experience</h2>
	<ul>
		{#each work as employer}
			<li class="employer">
				<h3>
					{employer.name}
				</h3>
				<ul>
					{#each employer.position as position}
						<li class="position">
							<div class="title-container">
								<h4 class="position-name">
									{position.name} • {employer.location}
								</h4>
								<span class="position-date">{position.start} - {position.end}</span>
							</div>
							<ul class="task-list">
								<li class="task-item">
									{#each position.task as task}
										<p class="task">
											{task}
										</p>
									{/each}
								</li>
							</ul>
						</li>
					{/each}
				</ul>
			</li>
		{/each}
	</ul>
</div>

<style>
	.employer,
	.position {
		list-style-type: none;
	}

	.position {
		margin-bottom: 2rem;
	}

	.employer {
		margin: 1rem 0;
	}

	.title-container {
		display: flex;
		align-items: center;
		justify-content: space-between;
		margin-bottom: 1rem;
	}

	.position-name {
		margin: 0;
		color: var(--color-primary-100);
	}

	.position-date {
		align-self: flex-end;
		color: var(--color-primary-100);
	}

	/* .task-list { */
	/* 	padding-left: 0.5rem; */
	/* } */

	.task-item {
		list-style-type: none;
		padding: 0;
		margin: 0.25rem 0;
	}

	.task {
		max-width: 40rem;
		margin: 0.25rem;
		line-height: 1.25;
		color: var(--color-primary-300);
	}
</style>
