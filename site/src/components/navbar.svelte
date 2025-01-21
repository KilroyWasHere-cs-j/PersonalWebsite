<script lang="ts">
	import { AppRail, AppRailAnchor, AppRailTile } from "@skeletonlabs/skeleton";
	import Icon from '../images/VudooLogo.svg';

    export let currentTile: number = 0;
</script>
<AppRail>
	<svelte:fragment slot="lead">
		<AppRailAnchor href="/" >
			<img src={Icon}/>
		</AppRailAnchor>
	</svelte:fragment>
	<!-- --- -->
	<AppRailTile bind:group={currentTile} name="tile-1" value={0} title="tile-1">
		<!-- <svelte:fragment slot="lead">(icon)</svelte:fragment> -->
		<span>Home</span>
	</AppRailTile>
	<AppRailTile bind:group={currentTile} name="tile-2" value={1} title="tile-2">
		<!-- <svelte:fragment slot="lead">(icon)</svelte:fragment> -->
		<span>Project</span>
	</AppRailTile>
	<AppRailTile bind:group={currentTile} name="tile-3" value={2} title="tile-3">
		<!-- <svelte:fragment slot="lead">(icon)</svelte:fragment> -->
		<span>More</span>
	</AppRailTile>
	<!-- --- -->
	<!-- <svelte:fragment slot="trail">
		<AppRailAnchor href="/" target="_blank" title="Account">nothing here</AppRailAnchor>
	</svelte:fragment> -->
</AppRail>