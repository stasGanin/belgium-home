<script>
  import { Phone } from "lucide-svelte";
</script>

<section
  id="hero"
  class="relative h-[90vh] flex items-center justify-center text-white"
  style="background-image: url('/images/roadSide.png'); background-size: cover; background-position: center;"
>
  <!-- Gradiënt overlay -->
  <div class="absolute inset-0 bg-gradient-to-b from-black/70 via-black/40 to-black/70"></div>

  <!-- Content -->
  <div class="relative z-10 px-6 max-w-3xl text-center">
    <div class="bg-black/40 backdrop-blur-sm rounded-2xl p-8 shadow-xl">
      <h1 class="text-4xl md:text-6xl font-extrabold mb-6 leading-tight">
        Uw droomhuis in België
      </h1>
      <p class="text-lg md:text-2xl mb-8 text-gray-200">
        Ruime en moderne woning in een gezellige buurt — klaar voor nieuwe eigenaars
      </p>
      <a
        href="#contact"
        class="inline-flex items-center gap-2 px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-xl text-white font-semibold shadow-lg transition"
      >
        <Phone size={22} /> Contacteer ons
      </a>
    </div>
  </div>
</section>
