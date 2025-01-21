<script lang="ts">
	import { AppBar, AppRail, AppRailAnchor, AppRailTile } from '@skeletonlabs/skeleton';
	import NavBar from '../../components/navbar.svelte';
	import Tri from '../../images/PurpleTri.png';
	import Navbar from '../../components/navbar.svelte';

	let projects = [
		{
			title: "Trinity Electrical System",
			body: "Body",
			url: "url"
		}
	]
	let slide = 0;
</script>


<div class="flex flex-row">
	<NavBar bind:currentTile={slide}/>
	<div class="flex flex-col justify-start w-screen h-screen space-y-4 text-white" style="
		background-image: url({Tri});
		background-size: cover;
		background-position: center;
		background-attachment: fixed;">

		{#if slide == 0 }
			<div class="flex flex-col space-y-4 m-4">
        		<h1 class="text-6xl text-white h-full motion-opacity-in-0 motion-delay-500 motion-duration-[2s]">What</h1>
        		<p class="text-2xl xl:w-[500px] h-full motion-opacity-in-0 motion-delay-500 motion-duration-[15s]">Lorem ipsum odor amet, consectetuer adipiscing elit. Et sem in luctus montes lacus mi enim vestibulum. Himenaeos dictum ad inceptos fermentum class amet maximus. Montes mi enim luctus nec, curae nisl efficitur. 
            		Cursus blandit maecenas semper in consectetur aenean montes ut. Consequat inceptos cras dis fames cursus ad.
	        	</p>
    	    	<div class="motion-opacity-in-0 motion-delay-500 motion-duration-[20s]">
        	    	<button type="button" class="btn variant-filled">Work with us</button>
        		</div>
    		</div>
    		<div class="flex justify-end space-y-4">
        		<div class="">
            		<h1 class="text-6xl text-white m-4 motion-opacity-in-0 motion-delay-500 motion-duration-[2s]">Different</h1>
            		<p class="text-2xl xl:w-[500px] h-full m-4 motion-opacity-in-0 motion-delay-500 motion-duration-[8s]">Lorem ipsum odor amet, consectetuer adipiscing elit. Et sem in luctus montes lacus mi enim vestibulum. Himenaeos dictum ad inceptos fermentum class amet maximus. Montes mi enim luctus nec, curae nisl efficitur. 
                		Cursus blandit maecenas semper in consectetur aenean montes ut. Consequat inceptos cras dis fames cursus ad.
            		</p>
        		</div>
    		</div>
    		<div class="flex justify-center motion-opacity-in-0 motion-delay-500 motion-duration-[11s]">
        		<h1 class="text-gray-900">Kilroy</h1>
    		</div>
		{/if}
    	{#if slide == 1}
			<div class="flex flex-col space-y-4 m-4">
				<div class="flex justify-end space-y-4">
					<div class="flex flex-col">
						<h1 class="text-6xl text-white h-full motion-opacity-in-0 motion-delay-500 motion-duration-[2s]">What</h1>
						<p class="text-2xl xl:w-[500px] h-full motion-opacity-in-0 motion-delay-500 motion-duration-[15s]">Lorem ipsum odor amet, consectetuer adipiscing elit. Et sem in luctus montes lacus mi enim vestibulum. Himenaeos dictum ad inceptos fermentum class amet maximus. Montes mi enim luctus nec, curae nisl efficitur. 
							Cursus blandit maecenas semper in consectetur aenean montes ut. Consequat inceptos cras dis fames cursus ad.
						</p>
						<div class="motion-opacity-in-0 motion-delay-500 motion-duration-[20s]">
							<button type="button" class="btn variant-filled">Work with us</button>
						</div>
					</div>
				</div>
			</div>
			<div class="flex justify-start space-y-4">
				<div class="">
					<h1 class="text-6xl text-white m-4 motion-opacity-in-0 motion-delay-500 motion-duration-[2s]">Different</h1>
					<p class="text-2xl xl:w-[500px] h-full m-4 motion-opacity-in-0 motion-delay-500 motion-duration-[8s]">Lorem ipsum odor amet, consectetuer adipiscing elit. Et sem in luctus montes lacus mi enim vestibulum. Himenaeos dictum ad inceptos fermentum class amet maximus. Montes mi enim luctus nec, curae nisl efficitur. 
						Cursus blandit maecenas semper in consectetur aenean montes ut. Consequat inceptos cras dis fames cursus ad.
					</p>
				</div>
			</div>
			<div class="flex justify-center motion-opacity-in-0 motion-delay-500 motion-duration-[11s]">
				<h1 class="text-gray-900">Kilroy</h1>
			</div>
		{/if}
		{#if slide == 2}
			<div class="grid grid-cols-4">
				<div class="card m-4 p-4">
					<h1 class="text-3xl">Title</h1>
					<h2></h2>
				</div>
			</div>
		{/if}
	</div>
</div>