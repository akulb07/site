<script>
    import Head from '$lib/components/layout/Head.svelte';
    import Blogs from '$lib/components/Blogs.svelte';
    import { onMount } from 'svelte'; // Import onMount to set the document title

    export let data;
    const posts = data.posts;
    const tags = data.tags;

    // Set the title for the page
    const pageTitle = "All Posts";

    // Set the document title when the component mounts
    onMount(() => {
        document.title = pageTitle; // Set the webpage title to "All Posts"
    });
</script>

<svelte:head>
    <title>{pageTitle}</title>
</svelte:head>

<Blogs title={pageTitle} {posts} {tags} />
