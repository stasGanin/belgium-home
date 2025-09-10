<script>
  let isOpen = false;

  // Blokkeer scroll van de site bij open modal
  

  function handleKeydown(e) {
    if (e.key === "Escape") {
      isOpen = false;
    }
  }
</script>

<section id="plan" class="py-16">
  <h2 class="text-3xl font-bold text-center mb-8">Plattegrond</h2>

  <div class="max-w-4xl mx-auto px-4">
    <button
      type="button"
      class="w-full"
      on:click={() => (isOpen = true)}
    >
      <img
        src="/images/plan.jpg"
        alt="Plattegrond van de woning"
        class="w-full max-h-[70vh] object-contain rounded-xl shadow-lg"
      />
    </button>
  </div>

  {#if isOpen}
    <!-- Modal -->
    <div
      class="fixed inset-0 bg-black/80 flex items-center justify-center z-50"
      role="dialog"
      aria-label="Plattegrond"
      tabindex="-1"
      on:click={() => (isOpen = false)}
      on:keydown={handleKeydown}
    >
      <div
        class="relative max-w-6xl w-full h-full flex justify-center overflow-y-auto p-8"
        on:click|stopPropagation
      >
        <!-- Grote afbeelding -->
        <img
          src="/images/plan.jpg"
          alt="Plattegrond van de woning"
          class="max-w-full h-auto rounded-xl shadow-xl"
          style="max-height: none;"
        />

        <!-- Sluitknop -->
        <button
          type="button"
          class="fixed top-6 right-6 bg-white/80 hover:bg-white text-black rounded-full p-2 shadow-md"
          on:click={() => (isOpen = false)}
        >
          ✕
        </button>
      </div>
    </div>
  {/if}
</section>
