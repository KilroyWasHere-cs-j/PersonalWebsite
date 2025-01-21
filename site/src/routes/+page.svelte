<script lang="ts">
	import { onMount } from "svelte";

	onMount(() => {
    const article = document.querySelector('article');
    if (article) {
      article.style.visibility = 'visible'; // Ensure article is visible on load
    }
    setTimeout(() => {
      window.location.href = '/home'; // Adjust this to your route
    }, 1000); // Timeout to allow full animation time
  });
</script>


<div class="w-screen h-screen">
	<div class="flex flex-col w-full h-full justify-center">
		<div class="flex flex-row w-full justify-center">
			<h1 class="text-6xl m-2 motion-opacity-in-0 motion-duration-[4s] motion-delay-500 motion-text-out-red-500">Vudoo</h1>
			<h1 class="text-6xl m-2 motion-opacity-in-0 motion-duration-[4s] motion-delay-1000">Group</h1>
		</div>
	</div>
</div>
