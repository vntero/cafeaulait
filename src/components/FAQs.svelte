<script>
    import SectionWrapper from "./SectionWrapper.svelte";

    // Define your gallery items here
    let galleryItems = [
        {
            src: "/assets/photo1.jpg",
            title: "Photo 1 Title",
        },
        {
            src: "/assets/photo2.jpg",
            title: "Photo 2 Title",
        },
        {
            src: "/assets/photo3.jpg",
            title: "Photo 3 Title",
        },
        {
            src: "/assets/photo4.jpg",
            title: "Photo 4 Title",
        },
        // Add more photos here
    ];
</script>

<SectionWrapper id="faqs">
    <div class="py-20 flex flex-col items-center justify-center">
        <div class="flex flex-col gap-2 mb-10">
            <br>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                Ein Einblick in unsere <span class="text-red-500">Welt</span>
            </h3>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
            {#each galleryItems as item}
                <div class="relative overflow-hidden rounded-lg shadow-lg">
                    <img src={item.src} alt={item.title} class="w-full h-auto object-cover" />
                    <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-60 text-white p-2 text-center">
                        <p>{item.title}</p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</SectionWrapper>

<style>
    .gallery-img {
        width: 100%;
        height: auto;
        object-fit: cover;
    }
    .gallery-item {
        position: relative;
        overflow: hidden;
        border-radius: 0.5rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }
    .gallery-item .title {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        background-color: rgba(0, 0, 0, 0.6);
        color: white;
        padding: 0.5rem;
        text-align: center;
    }
</style>
