<script context="module">
	export function preload({ params, query }) {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	export let posts;
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<div class="container">
	<div class="row">
		<div class="col-sm">
			<h1 class="display-2">Blog</h1>
		</div>
	</div>
	<div class="row">
		<div class="col-sm">
			<ul class="list-group">
				{#each posts as post}
					<!-- we're using the non-standard `rel=prefetch` attribute to
							tell Sapper to load the data for the page as soon as
							the user hovers over the link or taps it, instead of
							waiting for the 'click' event -->
					<li class="list-group-item"><a rel='prefetch' href='blog/{post.slug}'>{post.title}</a></li>
				{/each}
			</ul>
		</div>
	</div>
</div>