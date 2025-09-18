<script>
  import {
    BedDouble,
    Bath,
    Sun,
    DoorOpen,
    Home,
    Trees,
    Sofa,
    LayoutDashboard,
    ChevronLeft,
    ChevronRight,
  } from "lucide-svelte";

  const images = [
    { label: "Slaapkamer 1", icon: BedDouble, src: ["/images/bedroom1.jpg", "/images/bedroom1_1.jpg"] },
    { label: "Slaapkamer 2", icon: BedDouble, src: ["/images/bedroom2.jpg"] },
    { label: "Keuken", icon: Home, src: ["/images/kitchen.jpg"] },

    { label: "Badkamer", icon: Bath, src: ["/images/masterBathroom_1.jpg", "/images/masterBathroom_2.jpg", "/images/masterBathroom_3.jpg"] },
    { label: "Toilet", icon: Bath, src: ["/images/guestToilet.jpg"] },

    { label: "Woonkamer", icon: Sofa, src: ["/images/livingRoom_1.jpg", "/images/livingRoom_2.jpg"] },
    { label: "Ingang", icon: LayoutDashboard, src: ["/images/lobby_1.jpg", "/images/lobby_2.jpg", "/images/lobby_3.jpg"] },

    { label: "Garage", icon: DoorOpen, src: ["/images/garage_1.jpg", "/images/garage_2.webp"] },
    

    { label: "Inkomhal", icon: LayoutDashboard, src: ["/images/corridor_1.jpg", "/images/corridor_2.jpg", "/images/corridor_3.jpg", "/images/corridor_4.jpg"] },
    { label: "Centrale verwarming en wasplaats", icon: LayoutDashboard, src: ["/images/boilerRoom_1.jpg", "/images/boilerRoom_2.jpg"] },

    { label: "Terras", icon: Sun, src: ["/images/terrace.jpg"] },
    { label: "Straatkant", icon: Trees, src: ["/images/roadSideH.jpg"] },
  ];

  let active = images[0];
  let currentIndex = 0;

  function selectCategory(category) {
    active = category;
    currentIndex = 0;
  }

  function prev() {
    if (active.src.length > 1) {
      currentIndex = (currentIndex - 1 + active.src.length) % active.src.length;
    }
  }

  function next() {
    if (active.src.length > 1) {
      currentIndex = (currentIndex + 1) % active.src.length;
    }
  }
</script>

<section id="gallery" class="py-16 bg-gray-50">
  <h2 class="text-3xl font-bold text-center mb-12">Fotogalerij</h2>

  <div class="max-w-6xl mx-auto px-4">
    <!-- Мобилка: квадратные кнопки -->
<div class="flex gap-3 overflow-x-auto pb-4 md:hidden">
  {#each images as category}
    <button
      on:click={() => selectCategory(category)}
      class="flex-shrink-0 flex flex-col items-center justify-center w-14 h-14 sm:w-16 sm:h-16 rounded-lg shadow text-[10px] sm:text-xs font-medium transition
      {active.label === category.label 
        ? 'bg-blue-500 text-white' 
        : 'bg-white text-gray-700 hover:bg-gray-100'}"
    >
      <svelte:component this={category.icon} size={20} />
      {#if active.label === category.label}
        <span class="mt-1 leading-tight">{category.label}</span>
      {/if}
    </button>
  {/each}
</div>


    <!-- Десктоп: кнопки слева -->
    <div class="grid md:grid-cols-4 gap-8 items-start">
      <div class="hidden md:flex flex-col gap-4 md:col-span-1 max-h-[600px] overflow-y-auto pr-2">
        {#each images as category}
          <button
            on:click={() => selectCategory(category)}
            class="w-full flex items-center gap-3 px-4 py-3 rounded-xl shadow-md transition text-left
            {active.label === category.label 
              ? 'bg-gradient-to-r from-blue-100 to-blue-200 text-blue-800' 
              : 'bg-white hover:bg-gray-100'}"
          >
            <svelte:component this={category.icon} size={22} />
            <span class="font-medium">{category.label}</span>
          </button>
        {/each}
      </div>

      <!-- Фото -->
      <div class="md:col-span-3 flex justify-center relative">
        <img
          src={active.src[currentIndex]}
          alt={active.label}
          class="w-full max-h-[600px] object-contain rounded-2xl shadow-lg bg-white transition-opacity duration-300"
        />

        {#if active.src.length > 1}
          <!-- Навигация -->
          <button
            on:click={prev}
            class="absolute left-4 top-1/2 -translate-y-1/2 bg-black/50 text-white p-2 rounded-full hover:bg-black/70"
          >
            <ChevronLeft size={24} />
          </button>

          <button
            on:click={next}
            class="absolute right-4 top-1/2 -translate-y-1/2 bg-black/50 text-white p-2 rounded-full hover:bg-black/70"
          >
            <ChevronRight size={24} />
          </button>
        {/if}
      </div>
    </div>
  </div>
</section>
