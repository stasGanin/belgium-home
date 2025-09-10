<script>
  import { BedDouble, Bath, Sun, DoorOpen, Home, ChevronLeft, ChevronRight } from "lucide-svelte";

  const images = [
    { label: "Slaapkamer 1", icon: BedDouble, src: ["/images/bedroom1.png", "/images/bedroom1_1.png"] },
    { label: "Slaapkamer 2", icon: BedDouble, src: ["/images/bedroom2.png"] },
    { label: "Keuken", icon: Home, src: ["/images/kitchen.png"] },
    { label: "Badkamer", icon: Bath, src: ["/images/masterBathroom_1.png", "/images/masterBathroom_2.png", "/images/masterBathroom_3.png"] },
    { label: "Terras", icon: Sun, src: ["/images/terrace.png"] },
    { label: "Garage", icon: DoorOpen, src: ["/images/garage.png"] },
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

  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-4 gap-8 items-start">
    <!-- Knoppen links -->
    <div class="flex flex-col gap-4 md:col-span-1">
      {#each images as category}
        <button
          on:click={() => selectCategory(category)}
          class="flex items-center gap-3 px-4 py-3 rounded-xl shadow-md bg-white hover:bg-gray-100 transition text-left
          {active.label === category.label ? 'ring-2 ring-blue-500' : ''}"
        >
          <svelte:component this={category.icon} size={22} />
          <span class="font-medium">{category.label}</span>
        </button>
      {/each}
    </div>

    <!-- Foto rechts -->
    <div class="md:col-span-3 flex justify-center relative">
      <img
        src={active.src[currentIndex]}
        alt={active.label}
        class="w-full max-h-[600px] object-contain rounded-2xl shadow-lg bg-white transition-opacity duration-300"
      />

      {#if active.src.length > 1}
        <!-- Navigatie knoppen -->
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
</section>
