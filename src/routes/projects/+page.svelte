<script>
    import Title from '$lib/components/Title.svelte';
    import Card from '$lib/components/Card.svelte';
    import { onMount } from 'svelte'; // Import onMount to set the document title

    // Set the title for the page
    const pageTitle = "Projects";

    // Set the document title when the component mounts
    onMount(() => {
        document.title = pageTitle; // Set the webpage title to "Projects"
    });
</script>

<svelte:head>
    <title>{pageTitle}</title>
</svelte:head>

<div class="flex items-center justify-center">
    <div class="w-full max-w-6xl">
        <div class="space-y-2 pt-6 pb-8 md:space-y-5 text-center">
            <Title title={pageTitle} subtitle="Things that I'm currently working on." />
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
                <Card
                        title="site"
                        link="https://github.com/akulb07/site"
                        description="personal website"
                        class="p-6 md:p-8"
                />
                <Card
                        title="CompetitiveProgramming"
                        link="https://github.com/akulb07/CompetitiveProgramming"
                        description="Solutions to problems on platforms like CSES, LeetCode, etc."
                        class="p-6 md:p-8"
                />
            </div>
        </div>
    </div>
</div>
