<style>
		@media screen and (min-width: 576px) {
  		@supports ((perspective: 1px) and (not (-webkit-overflow-scrolling: touch))) {
			.parallax__group {
				position: relative;
				height: 100vh;
				transform-style: preserve-3d;
				margin-left: calc(100% - 100vw);
    			margin-right: calc(100% - 100vw);
    			padding-left: calc(100vw - 100%);
    			padding-right: calc(100vw - 100%);
				display: block;
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
			}
			.bg1, .bg2 {
				background-size: cover;
				background-repeat: no-repeat;
			}

			.bg1{
				background-image: url(images/dhmtrl.jpg);
			}
			.bg2{
				background-image: url(ascent.jpg);
			}
			#one{
				z-index: -1;
			}
			#two{
				z-index: 0;
				top: 969px;
			}
		}
	}
</style>

<svelte:head>
	<title>filbert.io</title>
</svelte:head>

<div class="parallax__group" id="one">
	<div class="container parallax__layer parallax__layer--base">
		<div class="row fixed-bottom">
			<div class="col-md jumbotron bg-dark">
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
	</div>
	<div class="parallax__layer parallax__layer--back bg1"></div>
</div>
<div class="parallax__group" id="two">
	<div class="container parallax__layer parallax__layer--base">
		<div class="row sticky-top">
			<div class="col-md jumbotron bg-dark">
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
	</div>
	<div class="parallax__layer parallax__layer--back bg2"></div>
</div>