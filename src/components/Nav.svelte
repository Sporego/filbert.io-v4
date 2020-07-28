<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1.5em;
		z-index: 1;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>


<nav class="navbar navbar-expand navbar-dark bg-dark sticky-top">
	<a class="navbar-brand" href=".">filbert.io</a>
	  <div class="navbar-nav">
		<a class="nav-item nav-link active" aria-current="{segment === undefined ? 'page' : undefined}" href=".">home </a>
		<a class="nav-item nav-link active" aria-current="{segment === 'projects' ? 'page' : undefined}" href="projects">projects</a>
		<a class="nav-item nav-link active" rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a>
	  </div>
  </nav>
