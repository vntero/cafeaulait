<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";

    let lim = true;

    let reviewsList = [
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
        {
            name: "Josette Stehli - Zuschauerin",
            review: `"Le Souffle est une histoire humaine qui remue l'âme au plus profond. Le coeur explose en émotions qui ne peuvent se cacher. Un cri, un seul, nous transperce... qui porte en lui tous les mots de toutes les langues de notre terre. Le mouvement, le rythme, le silence sont l'expression de cette force courageuse qui porte l'homme sur le sentier universel vers l'accueil de toute vie. Merci Café au Lait."`,
            features: [
                "Mouvement",
                "Humaine",
                "Force courageuse",
            ],
        },
        {
            name: "Zoe Venakis/Julia Bendlin - SRF",
            review: `"Café au Lait und ihre Macher schenken der Schweizer Kultur eine neue Dimension. Die Performance ist kraftvoll und laut, wie man es von afrikanischen Tänzen und Gesängen kennt."`,
            features: [
                "Gemeinschaft",
                "Kulturelle Vielfalt",
                "Tradition",
            ],
        },
        {
            name: "Zürcher Spendenparlament",
            review: `"Wir wurden dieses Jahr vom Zürcher Spendenparlament unterstützt. Wir bedanken uns herzlich beim Spendenparlament und bei unseren Künstlern Sahara und Omkar, die uns am Anlass repräsentiert haben."`,
            features: [
                "Ermächtigung",
                "Zusammenarbeit",
                "Stolz",
            ],
        },
        {
            name: "Klaus Merz - Schriftsteller",
            review: `"Die neue Produktion “Le Souffle” ist nicht nur herzzerreissend schön, sondern auch künstlerisch klug durchdacht. Flankiert von achtsamen Trommeln und Tänzern und ebenso virtuosem Gesang tanzen und atmen unsere Kinder und Menschenskinder – tragend und getragen – in der wogenden Schar."`,
            features: [
                "Herzzerreißend",
                "Künstlerisch",
                "Virtuos",
            ],
        },
        {
            name: "Max Pflüger - Ostschweiz am Sonntag",
            review: `"Erzählt bildhaft von Erlebnissen afrikanischer Migranten. Ohne Worte und dennoch ausdrucksstark."`,
            features: [
                "Ausdrucksstark",
                "Erlebnisse",
                "Bildhaft",
            ],
        },
    ];
</script>

<SectionWrapper id="reviews">
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
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Mehr anzeigen" : "Weniger anzeigen"}</p>
        </button>
    </div>
</SectionWrapper>