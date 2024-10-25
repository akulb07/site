<script>
    import Title from '$lib/components/Title.svelte';
    export let title = '';
    export let subtitle = '';
    export let posts = [];
    export let h2 = false;

    let searchQuery = '';
</script>

<style>
    .underline-animation {
        position: relative;
        display: inline-block;
    }

    .underline-animation:before {
        content: '';
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        height: 2px;
        background: linear-gradient(to right, #2563eb, #60a5fa);
        transform: scaleX(0);
        transform-origin: bottom right;
        transition: transform 0.3s ease-out;
    }

    .underline-animation:hover:before {
        transform: scaleX(1);
        transform-origin: bottom left;
    }

    .search-input {
        padding: 4px 8px;
        border: 1px solid transparent;
        border-bottom: 1px solid #ccc;
        background-color: transparent;
        color: inherit;
    }

    .search-input:focus {
        outline: none;
        box-shadow: none;
    }
</style>

<div class="flex justify-center items-center">
    <div class="w-full max-w-2xl divide-y divide-gray-200 dark:divide-gray-700">
        <div class="flex justify-between items-center pt-6 pb-8 space-y-2 md:space-y-5">
            <Title {title} {subtitle} {h2} class="underline-animation" />
            <input
                    type="text"
                    placeholder="Search posts..."
                    bind:value={searchQuery}
                    class="search-input"
            />
        </div>

        {#if !posts.filter(post => post.title.toLowerCase().includes(searchQuery.toLowerCase())).length}
            <p class="text-center py-4">No posts found.</p>
        {:else}
            <ul class="my-2">
                {#each posts.filter(post => post.title.toLowerCase().includes(searchQuery.toLowerCase())) as post}
                    <li class="py-4">
                        <div class="space-y-2">
                            <h2 class="text-2xl font-bold leading-8 tracking-tight">
                                <a href={`/blog/${post.slug}`} class="text-gray-900 dark:text-gray-100 underline-animation">
                                    {post.title}
                                </a>
                            </h2>
                            <p class="text-sm text-gray-600 dark:text-gray-400">{post.date}</p>
                        </div>
                    </li>
                {/each}
            </ul>
        {/if}
    </div>
</div>
