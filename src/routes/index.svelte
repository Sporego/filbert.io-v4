<style>
		@media screen and (min-width: 40em) {
  		@supports ((perspective: 1px) and (not (-webkit-overflow-scrolling: touch))) {
			.parallax__group {
				position: relative;
				height: 100vh;
				transform-style: preserve-3d;
				margin-left: calc(100% - 100vw);
    			margin-right: calc(100% - 100vw);
    			padding-left: calc(100vw - 100%);
    			padding-right: calc(100vw - 100%);
			}
			.parallax__layer {
				position: absolute;
				top: 0;
				right: 0;
				bottom: 0;
				left: 0;
			}
			.parallax__layer--base {
				transform: translateZ(0);
			}
			.parallax__layer--back {
				transform: translateZ(-1px) scale(2);
				z-index: -1;
			}
			.parallax__layer--deep {
				transform: translateZ(-2px) scale(3);
			}
		}
	}

	.bg1, .bg2 {
		background-size: cover;
    	background-repeat: no-repeat;
    	background-position: center;
	}

	.bg1{
		background-image: url(ascent.jpg);
	}
	.bg2{
		background-image: url(space.jpg);
	}

</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<div class="parallax__group">
	<div class="container parallax__layer parallax__layer--base">
		<div class="row">
			<div class="col-md jumbotron">
				<h2 class="display-4">filbert.io <span class="badge badge-secondary">New</span></h2>
				<p class="lead">Personal Portfolio Website</p>
				<hr class="my-4">
				<li>Built on Svelte</li>
				<li>Server-side Rendered</li>
				<li>Bandwidth Optimized</li>
				<p>It uses utility classes for typography and spacing to space content out within the larger container.</p> 	
				<a class="btn btn-primary btn-md" href="." role="button">Learn more</a>
			</div>
		</div>
	</div>>
	<div class="parallax__layer parallax__layer--back bg1"></div>
</div>