<script lang="ts">
    import Navbar from '../../components/navbar.svelte';
    import ProjectBox from '../../components/project.svelte';

    let showProjects = false;

    let projects = [
        {
            title: "Trinity Electrical Systems",
            body: "A complete redesign and rebuild of their website",
            date: "Currently building this",
            link: "https://trinity-electric.vercel.app/"
        },
        {
            title: "This website",
            body: "We made this",
            date: "Currently building this",
            link: "Your here"
        },
    ];
</script>

<Navbar />

<div class="flex flex-col justify-start w-screen h-screen bg-black">
    <div class="flex flex-col w-screen">
        <h1 class="flex justify-center text-white text-9xl m-4">Projects</h1>
    
        {#if !showProjects}
            <button class="w-screen md:h-[50px] bg-purple-900 rounded-xl m-4" onclick={() => showProjects = true}>See projects</button>
        {/if}
    </div>

    {#if showProjects}
        {#each projects as { title, body, date, link }, id}
            <ProjectBox title={title} body={body} date={date} link={link} delay={id}/>
        {/each}
    {/if}
</div>
