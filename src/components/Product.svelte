<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures=[
        {
            featureList: [
            ],
            description: 'Komplexe panafrikanische Tänze werden auf mittlerem bis fortgeschrittenem Niveau erarbeitet. Komplexe panafrikanische Tänze werden auf mittlerem bis fortgeschrittenem Niveau erarbeitet. Komplexe panafrikanische Tänze werden auf mittlerem bis fortgeschrittenem Niveau erarbeitet. Komplexe panafrikanische Tänze werden auf mittlerem bis fortgeschrittenem Niveau erarbeitet.',
            imgUrl: 'assets/afrotanz.png'
        },
    ]
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Kurse
            </h3>
        </div>
            {#each productFeatures as productFeature, index}
                <ProductCard {productFeature} {index} >
                    {#if index === 0}
                    We have many classes <span class="text-red-500 font-medium"> for all ages</span>
                    {:else if index === 1}
                    Afro <span class="text-red-500 font-medium">Beats</span>
                    {:else if index === 2}
                    Afro Beats <span class="text-red-500 font-medium">Masterclass</span>
                    {:else if index === 3}
                    Gospel<span class="text-red-500 font-medium">chor</span>
                    {:else}
                    Stage <span class="text-red-500 font-medium">Company</span>
                    {/if}
                </ProductCard>
            {/each}
        </div>
</SectionWrapper>