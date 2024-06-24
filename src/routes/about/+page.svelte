<script>
    import Title from '$lib/components/Title.svelte';
    let title = "About me";
    let friendsTitle = "My friends";
    let friendName = "Nermal";
    let friendGitHub = "https://github.com/nermalcat69";
    let friendImage = "https://eu-central.storage.cloudconvert.com/tasks/8fcb1d2d-4756-4e00-947d-5b0bfc220f09/73933669.webp?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=cloudconvert-production%2F20240525%2Ffra%2Fs3%2Faws4_request&X-Amz-Date=20240525T051356Z&X-Amz-Expires=86400&X-Amz-Signature=4eeca55d950c6fac7d250297348e73e6d3885c3bb44c7ce7bb7177059788dcab&X-Amz-SignedHeaders=host&response-content-disposition=inline%3B%20filename%3D%2273933669.webp%22&response-content-type=image%2Fwebp&x-id=GetObject";
</script>

<div class="flex justify-center items-center">
    <div class="w-full max-w-2xl divide-y divide-gray-200 dark:divide-gray-700">
        <div class="space-y-2 pt-6 pb-8 md:space-y-5">
            <div>
                <Title {title} />
            </div>
        </div>
        <div class="pt-8">
            <h1 class="text-2xl">Yeah...I don't really know what to write here.</h1>
        </div>
    </div>
</div>
