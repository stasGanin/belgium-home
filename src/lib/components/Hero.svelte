<script>
  import { Phone, Bed, Bath, Ruler, Square, Tag, Calendar } from "lucide-svelte";
</script>

<section
  id="hero"
  class="relative min-h-screen flex items-center justify-center text-white"
  style="background-image: url('/images/roadSide.jpg'); background-size: cover; background-position: center;"
>
  <!-- Overlay -->
  <div class="absolute inset-0 bg-black/50"></div>

  <!-- Content -->
  <div class="relative z-10 w-full px-4 sm:px-6 lg:px-8 pt-20 pb-12">
    <div class="max-w-4xl mx-auto text-center bg-black/40 backdrop-blur-sm rounded-2xl p-6 sm:p-10 shadow-xl">
      
      <!-- Заголовок -->
      <h1 class="text-3xl sm:text-5xl font-extrabold mb-4 leading-tight">
        Uw nieuwe droomwoning
      </h1>

      <!-- Подзаголовок -->
      <p class="text-base sm:text-lg md:text-xl mb-6 text-gray-200">
        Een luxueus en modern appartement, gelegen in een gezellige buurt — klaar voor nieuwe eigenaars.
      </p>

      <!-- Статы -->
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-6 mb-8 text-gray-200">
        <div class="flex flex-col items-center text-center">
          <Bed size={28} class="mb-1" />
          <span class="font-semibold">2 slaapkamers</span>
        </div>
        <div class="flex flex-col items-center text-center">
          <Bath size={28} class="mb-1" />
          <span class="font-semibold">1 badkamer</span>
        </div>
        <div class="flex flex-col items-center text-center">
          <Ruler size={28} class="mb-1" />
          <span class="font-semibold">99 m²</span>
          <span class="text-xs">bewoonbare ruimte</span>
        </div>
        <div class="flex flex-col items-center text-center">
          <Square size={28} class="mb-1" />
          <span class="font-semibold">14 m²</span>
          <span class="text-xs">terras</span>
        </div>
        <div class="flex flex-col items-center text-center">
          <Calendar size={28} class="mb-1" />
          <span class="font-semibold">Bouwjaar 2007</span>
        </div>
        <div class="flex flex-col items-center text-center">
          <span class="text-2xl sm:text-3xl font-extrabold text-green-400 mb-1">B</span>
          <span class="font-semibold">EPC</span>
        </div>
      </div>

      <!-- Цена -->
      <div class="mb-8">
        <Tag size={32} class="mb-2 text-green-400 mx-auto" />
        <p class="text-2xl sm:text-3xl md:text-4xl font-extrabold text-green-400">
          € 310.000
        </p>
        <p class="text-sm text-gray-200">Vraagprijs</p>
        <p class="text-xs sm:text-sm mt-2 text-gray-300 italic">
          Optie: ruilen met een huis in dezelfde prijscategorie
        </p>
      </div>

      <!-- Кнопка -->
      <a
        href="#contact"
        class="inline-flex items-center gap-2 px-6 py-3 sm:px-8 sm:py-4 bg-blue-600 hover:bg-blue-700 rounded-xl text-white font-semibold shadow-lg transition text-sm sm:text-base"
      >
        <Phone size={20} /> Contacteer ons
      </a>
    </div>
  </div>
</section>
