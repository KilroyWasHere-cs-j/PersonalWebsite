<script lang="ts">
	import Spacer from '../components/Spacer.svelte';
	import Item from '../components/Item.svelte';

	let points = ['First bullet point', 'Second bullet point', 'Third bullet point'];
</script>

<div class="h-screen w-full bg-black">
	<Spacer height="20px" />
	<h1 class="text-center text-9xl font-bold text-green-600 shadow-md shadow-green-600">
		~$ Gabriel Tower <span class="blinking-cursor"></span>
	</h1>

	<Spacer height="40px" />
	<h1 class="text-center text-6xl text-green-500">Whoiam</h1>
	<!-- <Underline /> -->
	<Spacer height="20px" />

	<h1 class="m-6 flex justify-center text-center text-6xl text-green-500">Projects</h1>
	<Item title="Web Browser" body="A basic W3M like terminal" tech="Rust" {points}></Item>
	<Item title="Database" body="A simple database written in Rust" tech="Rust" {points}></Item>
</div>

<style>
	.blinking-cursor {
		display: inline-block;
		width: 40px;
		height: 70px;
		background-color: green;
		opacity: 0.6;
		animation: blink 1s step-end infinite;
	}

	@keyframes blink {
		50% {
			opacity: 0;
		}
	}
</style>
