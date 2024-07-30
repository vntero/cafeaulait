<script>
    import ShowsCard from "./ShowsCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";

    let lim = true;

    let showsList = [
        {
            name: "Stadt Zürich",
            review: `"Die Stadt Zürich hat am 24. November 2023 Françoise Strassburg, Gründerin und Präsidentin von Café au Lait, und ihre Weggefährt:innen mit dem Kulturpreis 2023 im Bereich Tanz & Theater gewürdigt. Wir sind überglücklich über diesen Preis und bedanken uns bei der Stadt Zürich."`,
            features: [
                "Kulturpreis",
                "2023",
                "Tanz & Theater",
            ],
        },
        {
            name: "Zeno van Essel - stageplanet.ch",
            review: `"Ihre Wurzeln sind in Kamerun, Kongo, Togo, Kamerun, Jamaica und anderen Orten der Karibik, Afrikas und Asiens. Ihre Wurzeln sind aber auch hier in der Schweiz, dem Land, wo sie aufwachsen und dessen Dialekt sie sprechen. Zusammen bilden diese Kinder und Jugendlichen verschiedenster Hautfarbe, Herkunft und Kultur die Tanztruppe Café au Lait, die der Schweizer Kultur ein wichtiges Stück neuer, kraftvoller Authentizität hinzufügt."`,
            features: [
                "Authentizität",
                "Kultur",
                "Integration",
            ],
        },
    ];
</script>

<SectionWrapper id="shows">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <br>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
            Was andere über <span class="text-red-500">uns</span> sagen
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? showsList.slice(0, 4) : showsList as showsItem, index}
                    <ShowsCard {showsItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? showsList.slice(0, 4) : showsList as showsItem, index}
                    <ShowsCard {showsItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Mehr anzeigen" : "Weniger anzeigen"}</p>
        </button>
    </div>
</SectionWrapper>