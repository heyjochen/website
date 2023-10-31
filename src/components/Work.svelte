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
						'Developed IoT platform, seamlessly integrating 24/7 monitoring and real-time alerts to empower customers in maximizing their operational uptime.',
						'Reach out to and work with stakeholders to enhance UI/UX by leveraging robust design expertise'
					]
				},
				{
					name: 'Software Developer',
					start: 'Oct 2022',
					end: 'Nov 2023',
					task: [
						'Feature development in Vue.js, AngularJS, TypeScript',
						"Identified and solved issue with AngularJS's i18n solution by building internal tool to automate a manual process which improved developer experience, saving cost and effort"
					]
				}
			]
		},
		{
			name: '100Devs',
			location: 'Remote',
			position: [{ name: 'Software Engineer', start: 'Jan 2022', end: 'Oct 2022', task: [''] }]
		},
		{
			name: 'The Field Museum',
			location: 'Chicago, IL',
			position: [{ name: 'Studio Manager', start: 'Jun 2021', end: 'Jan 2022', task: [] }]
		}
	];
</script>

<div>
	<h4>Experience</h4>
	<ul>
		{#each work as employer}
			<li class="employer">
				<h5>
					{employer.name}
				</h5>
				<ul>
					{#each employer.position as position}
						<li class="position">
							<div class="title-container">
								<h6 class="position-name">
									{position.name} • {employer.location}
								</h6>
								<span class="position-date">{position.start} - {position.end}</span>
							</div>
							<ul class="task-list">
								{#each position.task as task}
									<li class="task">{task}</li>
								{/each}
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
	}

	.position-date {
		align-self: flex-end;
		color: var(--color-primary-200);
	}

	.task-list {
		padding-left: 1rem;
	}

	.task {
		list-style-type: circle;
		line-height: 1.25;
		padding-left: 0.5rem;
		margin: 0.25rem 0;
		color: var(--color-primary-200);
	}
</style>
