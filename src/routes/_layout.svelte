<script>
	import Nav from '../components/Nav.svelte';
	export let segment;


</script>

<style>
	body, html {
  		overflow: hidden;
	}
	body{
		transform-style: preserve-3d;
	}
	* {
    	margin: 0;
   		padding: 0;
	}
	@media screen and (min-width: 576px) {
  		@supports ((perspective: 1px) and (not (-webkit-overflow-scrolling: touch))) {
			/* ... parallax styles ... */
			#parallaxContainer {
				height: 100vh;
				overflow-x: hidden;
				overflow-y: auto;
				perspective: 1px;
				transform-style: preserve-3d;
			}


		
		}
	}
</style>

<div id="parallaxContainer">

	<Nav {segment}/>

	<slot/>

</div>