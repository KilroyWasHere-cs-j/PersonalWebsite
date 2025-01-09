<script lang="ts">
	import ProjBox from '../components/Project-box.svelte';
	import { goto } from '$app/navigation';

	let projects = [
		{
			title: 'Trinity Electrical Systems',
			body: 'Website contract with Trinity Electrical Systems rebuilding and redesigning their website',
			tech: 'Vercel, SvelteKit, TailwindCSS',
			points: ['Vercel', 'SvelteKit', 'TailwindCSS'],
			url: 'https://trinityelectricalsystems.com'
		},
		{
			title: 'Web Browser',
			body: 'A basic web browsers with VIM like bindings',
			tech: 'Rust',
			points: ['W3M with Vim like bindings', '', 'Third bullet point'],
			url: 'https://github.com/KilroyWasHere-cs-j/Sugar'
		},
		{
			title: 'Database',
			body: 'A cool database',
			tech: 'Rust',
			points: ['Rust', 'Cool db', 'Third bullet point'],
			url: 'https://github.com/KilroyWasHere-cs-j/NoSQLDatabase'
		},
		{
			title: 'RGNU',
			body: 'A rebuild of GNU tooling using Rust',
			tech: 'Rust',
			points: ['Rust', 'Cool compiler', 'Third bullet point'],
			url: 'https://github.com/nGNUr/nGNU'
		},
		{
			title: 'Software modem',
			body: 'A cool software modem',
			tech: 'Python',
			points: ['Python', 'Cool modem', 'Third bullet point'],
			url: 'https://github.com/KilroyWasHere-cs-j/AmMod'
		},
		{
			title: 'ScoutEye',
			body: 'A cool software modem',
			tech: 'Python',
			points: ['Python', 'OpenCV', 'Third bullet point'],
			url: 'https://github.com/KilroyWasHere-cs-j/ScoutEyeEX'
		},
		{
			title: 'Q-Learning',
			body: 'A cool software modem',
			tech: 'Python',
			points: ['Python', 'Q-Learning', 'Third bullet point'],
			url: 'https://github.com/KilroyWasHere-cs-j/QLearning'
		}
	]
</script>

<div class="flex flex-col items-center space-y-4 h-screen w-screen bg-black">
	<h1 class="text-center text-9xl font-bold text-green-600 shadow-md shadow-green-600">
		~$ Gabriel Tower <span class="blinking-cursor"></span>
	</h1>
	<h1 class="text-center text-6xl text-green-500">Whoiam</h1>

	<p class="m-4 text-center text-sm sm:text-base md:text-lg lg:text-xl text-green-500 max-w-3xl mx-auto px-4">
		By day I study Computer Information Systems at Wentworth Institute of Technology; by night I sleep. I'm too deep into the Rust hole now to turn back now, and I will eventually go full circle and program in C. I'm a FOSS and security diehard and believe that we have a right to own and understand the software we use. I will write any software for pretty much any purpose. 
	  
		I use Arch btw...
	</p>

	<h1 class="m-6 flex justify-center text-center text-6xl text-green-500">Projects</h1>

	<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-4 bg-black">
		{#each projects as project}
			<ProjBox title={project.title} body={project.body} tech={project.tech} points={project.points} url={project.url} /> 
		{/each}
	</div>
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
