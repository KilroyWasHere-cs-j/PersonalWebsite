<script lang="ts">
	export let title: string = '';
	export let body: string = '';
	export let tech: string = '';
	export let url: string = '';
	export let points: string[] = [];

	function navigateToUrl() {
		window.location.href = 'https://example.com'; // Replace with your URL
	}
</script>

<div class="m-4 mx-auto w-64 border-4 border-green-500">
	<div class="flex justify-center">
		<h1 class="text-green-500">{title}</h1>
		<p class="text-green-500">:</p>
		<p class="text-green-500">{tech}</p>
	</div>
	<div class="flex justify-center">
		<p class="m-2 text-green-500">{body}</p>
	</div>
	<div>
		<ul class="m-4 list-disc pl-6 text-green-500">
			{#each points as point}
				<li>{point}</li>
			{/each}
		</ul>
	</div>
	<button on:click={navigateToUrl} class="rounded bg-green-500 p-2 text-white"> Go to URL </button>
</div>
