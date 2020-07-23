<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	body, html {
  		overflow: hidden;
	}
	* {
    	margin: 0;
   		padding: 0;
	}
	@media screen and (min-width: 40em) {
  		@supports ((perspective: 1px) and (not (-webkit-overflow-scrolling: touch))) {
			/* ... parallax styles ... */
			.parallax {
				height: 100vh;
				overflow-x: hidden;
				overflow-y: auto;
				perspective: 300px;
			}


		
		}
	}
</style>

<div class="parallax">

	<Nav {segment}/>

	<slot/>

</div>