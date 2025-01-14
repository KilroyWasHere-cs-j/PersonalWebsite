<script lang="ts">
    export let title: string;
    export let body: string;
    export let date: string;
    export let link: string;
    export let delay: number;
</script>

<div class="flex flex-col justify-start space-y-4 border-2 rounded-xl motion-scale-in-0 motion-delay-[{delay}s] m-4 p-4">
    <h1 class="text-white text-4xl">{title}</h1>
    <p class="text-white">{body}</p>
    <p class="text-white">{date}</p>
    <!-- svelte-ignore a11y_consider_explicit_label -->
    <button 
        onclick={() => (window.location.href = link)}
        class="bg-white text-black rounded-xl md:w-[100px] md:h-[50px] border-2 p-2">
        Visit
    </button>
</div>