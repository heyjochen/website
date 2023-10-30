<script lang="ts">
	const work = [
		{
			name: 'nvisia',
			position: [
				{
					name: 'Software Engineer',
					start: 'Nov 2023',
					end: 'present',
					tasks: [
						'Developed IoT platform, seamlessly integrating 24/7 monitoring and real-time alerts to empower customers in maximizing their operational uptime.',
						'Reach out to and work with stakeholders to enhance UI/UX by leveraging robust design expertise'
					]
				},
				{
					name: 'Software Developer',
					start: 'Oct 2022',
					end: 'Nov 2023',
					tasks: [
						'Feature development in Vue.js, AngularJS, TypeScript',
						"Identified and solved issue with AngularJS's i18n solution by building internal tool to automate a manual process which improved developer experience, saving cost and effort"
					]
				}
			]
		}
	];
</script>

<div>
	<h2>Experience</h2>
	<ul>
		{#each work as item}
			<li>
				<h3>
					{item.name}
				</h3>
			</li>
		{/each}
	</ul>
</div>

<style>
</style>
