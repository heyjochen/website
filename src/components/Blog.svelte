<script lang="ts">
	import { formatDate } from '$lib/utils';
	// import * as config from '$lib/config';

	export let data;
</script>

<ul class="posts">
	{#each data.posts as post}
		<li class="post">
			<a href={`/blog/${post.slug}`} class="title">{post.title}</a>
			<!-- Updated link -->
			<p class="date">{formatDate(post.date)}</p>
			<p class="description">{post.description}</p>
		</li>
	{/each}
</ul>
