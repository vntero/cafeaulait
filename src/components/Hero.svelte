<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import Header from "./Header.svelte";
    import CTAs from "./CTAs.svelte";

    // Example events
    let events = [
        {
            date: "14.09.2024",
            title: "Afro Family Day",
            location: "GZ Buchegg, Zürich",
        },
        {
            date: "17.11.2024",
            title: `Premiere "R'Evolution" - Save the date!`,
            location: "Volkshaus, Zürich",
        },
    ];
</script>

<SectionWrapper>
    <Header />
    <div class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14">
        <h2 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold">
            Café au Lait
        </h2>
        <p class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">
            <span class="italic">Die Afrotanzgruppe aus Zürich für Kinder & Jugendliche</span>
        </p>

        <!-- Main image -->
        <img src="/assets/afrosummerjam.png" alt="Kinder" class="w-full max-w-[1000px] mx-auto rounded-lg shadow-md" />

        <CTAs />

        <!-- Upcoming Events Section -->
        <div class="max-w-[1000px] mx-auto w-full text-center bg-[#FFF1DB] p-6 rounded-lg shadow-lg">
            <h3 class="text-4xl font-semibold mb-6">Upcoming Events</h3>
            <ul class="list-disc list-inside text-left mx-auto max-w-lg">
                {#each events as event}
                    <li class="mb-4">
                        <span class="font-semibold">{event.date}</span>: {event.title} <br />
                        <span class="italic">{event.location}</span>
                    </li>
                {/each}
            </ul>
        </div>

        <div class="flex items-center justify-center gap-2 text-base">
            <p>4.9</p>
            {#each [0, 1, 2, 3, 4] as index}
                <div class="grid place-items-center relative">
                    <i class="fa-solid fa-star opacity-0"></i>
                    <div class={"absolute top-0 left-0 grid place-items-center " + (index === 4 ? "w-[60%] overflow-hidden" : " ")}>
                        <i class="fa-solid fa-star text-amber-400"></i>
                    </div>
                </div>
            {/each}
            <p>500+</p>
        </div>
    </div>
</SectionWrapper>
