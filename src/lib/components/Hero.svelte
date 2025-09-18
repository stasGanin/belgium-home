<script>
  import { Phone, Bed, Bath, Ruler, Square, Tag } from "lucide-svelte";
</script>

<section
  id="hero"
  class="relative h-[90vh] flex items-center justify-center text-white"
  style="background-image: url('/images/roadSide.jpg'); background-size: cover; background-position: center;"
>
  <!-- Gradiënt overlay -->
  <div class="absolute inset-0 bg-gradient-to-b from-black/70 via-black/40 to-black/70"></div>

  <!-- Content -->
  <div class="relative z-10 px-6 max-w-3xl text-center">
    <div class="bg-black/40 backdrop-blur-sm rounded-2xl p-8 shadow-xl">
      <h1 class="text-4xl md:text-6xl font-extrabold mb-6 leading-tight">
        Uw nieuwe droomwoning
      </h1>
      <p class="text-lg md:text-2xl mb-8 text-gray-200">
        Een luxueus en modern appartement, gelegen in een gezellige buurt — wachtend op zijn nieuwe eigenaars.
      </p>

      <!-- Info row -->
      <div class="grid grid-cols-2 gap-4 md:grid-cols-5 mb-8 text-gray-200">
        <div class="flex flex-col items-center">
          <Bed size={28} class="mb-1" />
          <span class="font-semibold">2 slaapkamers</span>
        </div>
        <div class="flex flex-col items-center">
          <Bath size={28} class="mb-1" />
          <span class="font-semibold">1 badkamer</span>
        </div>
        <div class="flex flex-col items-center">
          <Ruler size={28} class="mb-1" />
          <span class="font-semibold">99 m²</span>
          <span class="text-xs">bewoonbare ruimte</span>
        </div>
        <div class="flex flex-col items-center">
          <Square size={28} class="mb-1" />
          <span class="font-semibold">14 m²</span>
          <span class="text-xs">terras</span>
        </div>
        <div class="flex flex-col items-center">
          <Tag size={28} class="mb-1 text-green-400" />
          <span class="font-semibold">€ 310.000</span>
          <span class="text-xs">Vraagprijs</span>
        </div>
      </div>

      <a
        href="#contact"
        class="inline-flex items-center gap-2 px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-xl text-white font-semibold shadow-lg transition"
      >
        <Phone size={22} /> Contacteer ons
      </a>
    </div>
  </div>
</section>
