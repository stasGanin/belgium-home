<script>
  import { Menu } from "lucide-svelte";

  let isOpen = false;

  const links = [
    { href: "#hero", label: "Home" },
    { href: "#gallery", label: "Fotogalerij" },
    { href: "#plan", label: "Plan" },
    { href: "#description", label: "Beschrijving" },
    { href: "#contact", label: "Contact" }
  ];
</script>

<header class="fixed top-0 left-0 w-full bg-white/80 backdrop-blur-md shadow z-50">
  <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
    <!-- Logo -->
    <a href="#hero" class="text-2xl font-bold text-blue-600">Belgium Home</a>

    <!-- Desktop nav -->
    <nav class="hidden md:flex gap-8">
      {#each links as { href, label }}
        <a
          href={href}
          class="text-gray-700 hover:text-blue-600 transition font-medium"
        >
          {label}
        </a>
      {/each}
    </nav>

    <!-- Mobile burger -->
    <button
      class="md:hidden text-gray-700"
      on:click={() => (isOpen = !isOpen)}
    >
      <Menu size={28} />
    </button>
  </div>

  <!-- Mobile menu -->
  {#if isOpen}
    <nav class="md:hidden bg-gray-100/90 backdrop-blur px-6 py-4 space-y-4">
      {#each links as { href, label }}
        <a
          href={href}
          on:click={() => (isOpen = false)}
          class="block text-gray-700 hover:text-blue-600 transition font-medium"
        >
          {label}
        </a>
      {/each}
    </nav>
  {/if}
</header>

<style>
  html {
    scroll-behavior: smooth;
  }
</style>
