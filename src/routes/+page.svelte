
<div class="min-h-screen {bgColor} p-8 text-{textColor}">
    <h1 class="text-6xl font-extrabold ">Boden Harris</h1>
    <button 
    class="absolute w-16 h-16 top-4 right-4 flex items-center justify-center rounded-full {bgColor} hover:{hoverColor} focus:outline-none focus:ring-2 focus:ring-blue-500 transition"
    aria-label="Toggle Night Mode"
    on:click={toggleNightMode}>
        <img src="moonClipart.png" alt="Moon Icon" class="w-[48px] h-[48px]">
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
<script>
    let nightMode = true;
    let bgColors = [
        'bg-gray-300', 'bg-gray-800'
    ];
    let textColors = [
        'text-gray-800', 'white'
    ];
    let borderColors = [
        'border-gray-800', 'border-gray-500'
    ];
    let hoverColors = [
        'border-gray-200', 'border-gray-700'
    ];
    let bgColor = bgColors[1];
    let textColor = textColors[1];
    let borderColor = borderColors[1];
    let hoverColor = hoverColors[1];

    function toggleNightMode() {

       if (nightMode) {
        bgColor = bgColors[0];
        textColor = textColors[0];
        borderColor = borderColors[0]; 
        hoverColor = hoverColors[0];
       } else {
        bgColor = bgColors[1];
        textColor = textColors[1];
        borderColor = borderColors[1]; 
        hoverColor = hoverColors[1];
       }
       nightMode=!nightMode;
    }
</script>

