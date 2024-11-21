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

<div class="m-4 mx-auto w-64 border-4 border-green-500 rounded-lg">
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
	<div class="flex justify-center m-4">
		<a href="{url}"
		class="px-4 py-2 text-white-500 bg-green-500 rounded-xl hover:text-white-500">Vist Project Source</a>
	</div>
</div>
