<script>
    import Title from '$lib/components/Title.svelte';
    import Gallery from '$lib/components/Gallery.svelte';
    import { onMount } from 'svelte'; // Import onMount to set the document title

    // Import images
    import psone from '$lib/assets/problemsolvingbasic.png';
    import pythonbasic from '$lib/assets/pythonbasic.png';
    import sqlbasic from '$lib/assets/sqlbasic.png';
    import javascriptintermediate from '$lib/assets/javascriptintermediate.png';
    import softwarengineer from '$lib/assets/softwareengineerintern.png';

    // Set the title for the page
    const pageTitle = "Gallery";

    // Set the document title when the component mounts
    onMount(() => {
        document.title = pageTitle; // Set the webpage title to "Gallery"
    });
</script>

<svelte:head>
    <title>{pageTitle}</title>
</svelte:head>

<div class="flex items-center justify-center">
    <div class="divide-y divide-gray-200 dark:divide-gray-700">
        <div class="space-y-2 pt-6 pb-8 md:space-y-5 text-center">
            <Title title={pageTitle} /> <!-- Pass the page title to the Title component -->
        </div>
    </div>
</div>

<div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 gap-4">
        <Gallery
                imgSrc={softwarengineer}
                alt="Hackerrank software engineer intern certification"
                certificationText="Hackerrank Software Engineer Intern certification"
                link="https://www.hackerrank.com/profile/batraakul"
        />
        <Gallery
                imgSrc={javascriptintermediate}
                alt="JavaScript intermediate certification"
                certificationText="Hackerrank JavaScript (Intermediate) certification"
                link="https://www.hackerrank.com/profile/batraakul"
        />
        <Gallery
                imgSrc={psone}
                alt="Problem Solving Intermediate certification"
                certificationText="Hackerrank Problem Solving (Intermediate) certification"
                link="https://www.hackerrank.com/profile/batraakul"
        />
        <Gallery
                imgSrc={sqlbasic}
                alt="SQL basic certification"
                certificationText="Hackerrank SQL (Basic) certification"
                link="https://www.hackerrank.com/profile/batraakul"
        />
        <Gallery
                imgSrc={pythonbasic}
                alt="Python certification"
                certificationText="Hackerrank Python (Basic) certification"
                link="https://www.hackerrank.com/profile/batraakul"
        />
    </div>
</div>
