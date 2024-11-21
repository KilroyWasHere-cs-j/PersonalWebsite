<script lang="ts">
	import Spacer from '../components/Spacer.svelte';
	import Item from '../components/Item.svelte';
	import { goto } from '$app/navigation';

	let wbPoints = ['W3M with Vim like bindings', '', 'Third bullet point'];
	let wbURL = "https://github.com/KilroyWasHere-cs-j/Sugar";

	let dbPoints = ['Rust', 'Cool db', 'Third bullet point'];
	let dbURL = "https://github.com/KilroyWasHere-cs-j/NoSQLDatabase";

	let nGNUPoints = ['Rust', 'FOSS', 'Third bullet point'];
	let nGNUURL = "https://github.com/nGNUr/nGNU";

	let amModPoints = ['Python', 'FSK', 'Third bullet point'];
	let amModURL = "https://github.com/KilroyWasHere-cs-j/AmMod";

	let scoutEyePoints = ['Python', 'OpenCV', 'Third bullet point'];
	let scoutEyeURL = "https://github.com/KilroyWasHere-cs-j/ScoutEyeEX";

	let qLearningPoints = ['Python', 'Q-Learning', 'Third bullet point'];
	let qLearningURL = "https://github.com/KilroyWasHere-cs-j/QLearning";
</script>

<div class="min-h-screen w-full bg-black">
	<Spacer height="20px" />
	<h1 class="text-center text-9xl font-bold text-green-600 shadow-md shadow-green-600">
		~$ Gabriel Tower <span class="blinking-cursor"></span>
	</h1>

	<Spacer height="40px" />
	<h1 class="text-center text-6xl text-green-500">Whoiam</h1>

	<p class="m-4 text-center text-sm sm:text-base md:text-lg lg:text-xl text-green-500 max-w-3xl mx-auto px-4">
		By day I study Computer Information Systems at Wentworth Institute of Technology; by night I sleep. I'm too deep into the Rust hole now to turn back now, and I will eventually go full circle and program in C. I'm a FOSS and security diehard and believe that we have a right to own and understand the software we use. I will write any software for pretty much any purpose. 
	  
		I use Arch btw...
	  </p>
	  
	<Spacer height="20px" />

	<h1 class="m-6 flex justify-center text-center text-6xl text-green-500">Projects</h1>

	<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-4">
		<Item title="Web Browser" body="A basic W3M like terminal" tech="Rust" points={wbPoints} url={wbURL} />
		<Item title="Database" body="A simple database written in Rust" tech="Rust" points={dbPoints} url={dbURL} />
		<Item title="nGNU" body="Contributed to a group project rewriting GNU" tech="Rust" points={nGNUPoints} url={nGNUURL} />
		<Item title="AmMod" body="A simple basic implementation of FSK" tech="Python" points={amModPoints} url={amModURL} />
		<Item title="ScoutEye" body="A crossplatform data collection tool for FRC" tech="C#" points={scoutEyePoints} url={scoutEyeURL} />
		<Item title="Q-Learning" body="A simple Q-Learning implementation" tech="Python" points={qLearningPoints} url={qLearningURL} />
	</div>

	<Spacer height="20px" />

	<div class="flex justify-center">
		<h1 class="">Contact</h1>
		<a href="https://github.com/KilroyWasHere-cs-j" class="text-green-500 hover:text-green-500">GitHub</a>	
		<div class="w-4"></div>
		<a href="#" class="text-green-500 hover:text-green-500">Personal Website</a>
		<div class="w-4"></div>
		<a href="mailto:gmtower1@proton.me" class="text-green-500">Email</a>		  
	</div>

	<button on:click={() => goto('/crypt')} class="bg-black-500 text-black-100 px-6 py-3 rounded hover:bg-black-700">
		Crypt
	</button>
	<button on:click={() => goto('/about')} class="bg-black-500 text-black-100 px-6 py-3 rounded hover:bg-black-700">
		About
	</button>
	<button on:click={() => goto('/JH')} class="bg-black-500 text-black-100 px-6 py-3 rounded hover:bg-black-700">
		Home
	</button>
</div>

<style>
	.blinking-cursor {
		display: inline-block;
		width: 40px;
		height: 80px;
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
