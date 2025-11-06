<script>
  import SectionWrapper from './SectionWrapper.svelte'

  let team = [
    {
      name: 'Françoise Strassburg',
      role: 'Gründerin',
      img: '/assets/pics/francoise.png',
    },
    {
      name: 'Amélie Aragón Kpenou',
      role: 'Co-Leiterin & Gesangsleiterin',
      img: '/assets/pics/amelie.png',
    },
    {
      name: 'Sahara Kuhn',
      role: 'Co-Leiterin & Tanzpädagogin Afrobeats',
      img: '/assets/pics/sahara.png',
    },
    {
      name: 'Deniz Tunbeceren',
      role: 'Koordinatorin Events & Sponsoring',
      img: '/assets/pics/deniz.png',
    },
    {
      name: 'Akim Princes',
      role: 'Tanzpädagoge traditioneller Tanz',
      img: '/assets/pics/akim.png',
    },
    {
      name: 'Flora Luvualu',
      role: 'Gesangspädagogin',
      img: '/assets/pics/flora.png',
    },
    {
      name: 'Urbain Guiguemdé',
      role: 'Theaterpädagoge',
      img: '/assets/pics/urbain.png',
    },
    {
      name: 'Sékou Touré',
      role: 'Perkussionist',
      img: '/assets/pics/sekou.png',
    },
    {
      name: 'Yamoussa Sylla',
      role: 'Perkussionist',
      img: '/assets/pics/yamoussa.png',
    },
  ]
</script>

<!-- Unser Team -->
<SectionWrapper id="team">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Unser <span class="text-red-500">Team</span>
      </h3>
    </div>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 md:gap-14 w-full"
    >
      {#each team as member}
        <div
          class="flex flex-col gap-2 text-left max-w-[400px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <div class="flex items-center gap-4">
            <img
              src={member.img}
              alt={member.name}
              class="w-20 h-20 rounded-full object-cover shadow-md"
            />
            <h4 class="text-lg sm:text-xl md:text-2xl pt-2 text-red-500">
              {member.name}
            </h4>
          </div>
          <p class="pl-2">{member.role}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
