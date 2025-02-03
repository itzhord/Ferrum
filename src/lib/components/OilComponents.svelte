<script lang="ts">
    import Pump from '$lib/assets/oil tools/pump.jpg';
    import Valve from '$lib/assets/oil tools/valves.jpeg';
    import Compressor from '$lib/assets/oil tools/compressor.jpeg';
    import Sensor from '$lib/assets/oil tools/sensor.jpg';
    import Controls from '$lib/assets/oil tools/control system.jpg';
    import Safety from '$lib/assets/oil tools/safety.jpeg';
</script>

<div class="flex flex-col w-[90vw] gap-[2rem] m-[3.5rem]">
    <div class="flex flex-row w-[100%] overflow-hidden gap-[2rem]">
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Pump} 
                    alt="Pump" 
                    class="w-full h-full object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Pump</h1>
        </div>
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Valve} 
                    alt="Valves" 
                    class="w-full h-full object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Valves</h1>
        </div>
    </div>
    <div class="flex flex-row w-[100%] overflow-hidden gap-[2rem]">
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Compressor} 
                    alt="Compressor" 
                    class="w-full  object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center h-[65vh]" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Compressor</h1>
        </div>
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Sensor} 
                    alt="Sensor" 
                    class="w-full  object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center h-[65vh]" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Sensor</h1>
        </div>
    </div>
    <div class="flex flex-row w-[100%] overflow-hidden gap-[2rem]">
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Controls} 
                    alt="Controls" 
                    class="w-full object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center h-[65vh]" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Controls</h1>
        </div>
        <div class="relative group flex flex-col w-[50%] overflow-hidden rounded-xl">
            <div class="overflow-hidden rounded-xl relative">
                <img 
                    src={Safety} 
                    alt="Safety" 
                    class="w-full object-cover rounded-xl transition-transform duration-300 ease-in-out group-hover:scale-125 origin-center h-[65vh]" 
                />
            </div>
            <h1 class="text-[1.5rem] font-semibold mt-[1rem] text-left">Safety</h1>
        </div>
    </div>
</div>