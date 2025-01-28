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
    $: nightModeIcon = nightMode ? 'moonClipart.png' : 'sunClipart-removebg-preview.png';

    function toggleNightMode() {
        nightMode = !nightMode;
    }
</script>

<div class="min-h-screen {bgColor} p-8 {textColor}">
    <h1 class="text-6xl font-extrabold">Boden Harris</h1>
    <button 
    class="absolute w-16 h-16 top-4 right-4 flex items-center justify-center rounded-full {bgColor} {hoverColor} focus:outline-none focus:ring-2 focus:ring-blue-500 transition"
    aria-label="Toggle Night Mode"
    on:click={toggleNightMode}>
        <img src={nightModeIcon} alt="Moon Icon" class="w-[48px] h-[48px]">
    </button>
    <hr class="border-t-2 {borderColor}">
    <h2 class="text-lg ">blharris@umass.edu</h2>
    <p class=" mt-4 border {borderColor} rounded-lg w-1/2 h-auto p-3" >
        <b class="font-bold text-2xl">About me: </b><br>
        I am a freshman at the UMass Amerst Commonwealth Honors College studying Computer science. I am currently on track to graduate in the winter of 2026. 
    </p>
    <a href="Boden Harris - Resume.pdf" class="text-blue-400 mt-4 inline-block hover:text-blue-600">
        View My Resume
    </a>
</div>


