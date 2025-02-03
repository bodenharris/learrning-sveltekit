<script>
    let nightMode = true;

    const bgColors = ['bg-gray-300', 'bg-gray-800'];
    const textColors = ['text-gray-800', 'text-white'];
    const borderColors = ['border-gray-800', 'border-gray-500'];
    const hoverColors = ['hover:bg-gray-200', 'hover:bg-gray-700'];

    $: bgColor = nightMode ? bgColors[1] : bgColors[0];
    $: textColor = nightMode ? textColors[1] : textColors[0];
    $: borderColor = nightMode ? borderColors[1] : borderColors[0];
    $: hoverColor = nightMode ? hoverColors[1] : hoverColors[0];
    $: nightModeIcon = nightMode ? 'moonClipart.png' : 'sunClipart.png';

    function toggleNightMode() {
        nightMode = !nightMode;
    }

    function downloadResume() {
        const link = document.createElement('a');
        link.href = 'Boden Harris - Resume.pdf';
        link.download = 'Boden Harris - Resume.pdf';
        link.click();
    }

</script>

<div class="min-h-screen {bgColor} p-8 {textColor}">
    <h1 class="text-6xl font-extrabold">Boden Harris</h1>
    <button 
    class="absolute w-16 h-16 top-4 right-4 flex items-center justify-center rounded-full {bgColor} {hoverColor} focus:outline-none focus:ring-2 focus:ring-blue-500 transition"
    aria-label="Toggle Night Mode"
    on:click={toggleNightMode}>
        <img src={nightModeIcon} alt="Moon Icon" class="w-[48px] h-[48px]" style="{nightMode ? 'filter: invert(1)' : ''}">
    </button>
    <hr class="border-t-2 {borderColor}">
    <h2 class="text-lg ">blharris@umass.edu</h2>
    <p class=" mt-4 border {borderColor} rounded-lg w-1/2 h-auto p-3" >
        <b class="font-bold text-2xl">About me: </b><br>
        I am a freshman at the UMass Amerst Commonwealth Honors College studying Computer science.<br>I am currently on track to graduate in the winter of 2026. 
    </p>
    <button class = "absolute right-2 top-25 rounded-full h-96 w-96 hover:ring-2 ring-grey-500 transition">    
        <img src="profile.jpg" alt="" class="h-96 w-96 rounded-full">
    </button>
    <p class="mt-4 border {borderColor} rounded-lg w-1/2 h-auto p-1 flex items-center space-x-2">
        <a href="Boden Harris - Resume.pdf" class="text-blue-400 inline-block hover:text-blue-600 p-3" target="_blank">
            View My Resume
        </a> 
        <button 
        class="w-12 h-12 flex items-center justify-center rounded-full {bgColor} {hoverColor} focus:outline-none focus:ring-2 focus:ring-blue-500"
        aria-label="Download Resume"
        on:click={downloadResume}>
            <img src="downloadIcon.png" alt="Download Icon" class="w-[32px] h-[32px]" style="{nightMode ? 'filter: invert(1)' : ''}">
        </button>
    </p>
  
</div>


