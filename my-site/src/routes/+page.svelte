<script lang="ts">
    import { onMount } from "svelte";

    onMount(() => {
        const article = document.querySelector('article');
        if (article) {
            article.style.visibility = 'visible';
        }
        setTimeout(() => {
            window.location.href = '/home';
        }, 3000);
    });
</script>

<div class="flex flex-col justify-center w-screen h-screen bg-black">
    <div class="flex flex-row justify-center space-x-4 text-6xl">
        <h1 class="text-purple-900 motion-opacity-in-0 motion-duration-200 motion-delay-[1s]">Voodu</h1>
        <h1 class="text-green-700 motion-opacity-in-0 motion-duration-200 motion-delay-[2s]">Software</h1>
        <h1 class="text-white motion-opacity-in-0 motion-duration-200 motion-delay-[3s]">.</h1>
    </div>
</div>
