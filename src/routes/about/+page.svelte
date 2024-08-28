<script>
    import Title from '$lib/components/Title.svelte';
    let title = "About me";
    let trackTitle = "u ";
    let artist = "Kendrick Lamar";
    let albumCover = "https://lastfm.freetls.fastly.net/i/u/770x0/86b35c4eb3c479da49c915d8771bbd1a.jpg#86b35c4eb3c479da49c915d8771bbd1a";
    let spotifyLink = "https://open.spotify.com/track/1bxEpNR75Hq3T2oF9AZjt8?si=80ffc94f83094d24";
</script>

<div class="flex justify-center items-center">
    <div class="w-full max-w-2xl  divide-gray-200 dark:divide-gray-700">
        <div class="space-y-2 pt-6 pb-8 md:space-y-5">
            <div>
                <Title {title} />
            </div>
        </div>
        <div class="pt-8">
            <h1 class="text-2xl">.</h1>
        </div>
        <div class="pt-8">
            <div class=" rounded-lg  p-6 flex items-center space-x-6">
                <img src={albumCover} alt="Album cover" class="w-32 h-32 "/>
                <div>
                    <h2 class="text-lg font-medium text-gray-900 dark:text-gray-100">{trackTitle}</h2>
                    <p class="text-gray-500 dark:text-gray-400">{artist}</p>
                    <a href={spotifyLink} target="_blank" class="text-blue-500 dark:text-blue-400 hover:underline">Listen on Spotify</a>
                </div>
            </div>
        </div>
    </div>
</div>
