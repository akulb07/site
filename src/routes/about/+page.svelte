<script>
    import { onMount } from 'svelte';
    import Title from '$lib/components/Title.svelte';

    // Set the title for the page
    let title = "About";

    // Set the document title when the component mounts
    onMount(() => {
        document.title = title; // Set the webpage title to "About"
    });
</script>

<div class="flex justify-center items-center">
    <div class="w-full max-w-2xl divide-gray-200 dark:divide-gray-700">
        <div class="space-y-2 pt-6 pb-8 md:space-y-5">
            <div>
                <Title {title} />
            </div>
        </div>
        <div class="pt-8">
            <h1 class="text-2xl">Definitely one of the people of all time</h1>
        </div>
        <!-- Links Section -->
        <div class="pt-8">
            <h2 class="text-xl font-bold">Links</h2>
            <ul class="list-disc list-inside">
                <li>
                    <a href="https://github.com/akulb07" target="_blank" class="text-blue-500 hover:underline">
                        GitHub
                    </a>
                </li>
                <li>
                    <a href="https://lichess.org/@/akulb07" target="_blank" class="text-blue-500 hover:underline">
                        Lichess
                    </a>
                </li>
                <li>
                    <a href="https://www.hackerrank.com/profile/batraakul" target="_blank" class="text-blue-500 hover:underline">
                        HackerRank
                    </a>
                </li>
                <li>
                    <a href="https://leetcode.com/u/BatraAkul/" target="_blank" class="text-blue-500 hover:underline">
                        LeetCode
                    </a>
                </li>
            </ul>
        </div>
    </div>
</div>
