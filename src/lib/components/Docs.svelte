<script>
  import { FileText } from "lucide-svelte";
</script>

<section id="certificates" class="py-16 bg-gray-50">
  <div class="max-w-4xl mx-auto px-4 text-center">
    <h2 class="text-3xl font-bold mb-6">Certificaten</h2>
    <p class="mb-8 text-gray-600">
      Raadpleeg de officiële documenten van het huis:
    </p>

    <div class="flex flex-col md:flex-row justify-center gap-6">
      <!-- EPC Certificaat -->
      <a
        href="/docs/EPC_Certificaat.pdf"
        target="_blank"
        rel="noopener noreferrer"
        class="flex items-center gap-2 px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white rounded-xl shadow transition"
      >
        <FileText size={20} /> EPC Certificaat
      </a>

      <!-- Keuring van elektrische installatie -->
      <a
        href="/docs/Keuring van elektrische installatie.pdf"
        target="_blank"
        rel="noopener noreferrer"
        class="flex items-center gap-2 px-6 py-3 bg-gray-800 hover:bg-gray-900 text-white rounded-xl shadow transition"
      >
        <FileText size={20} /> Keuring elektrische installatie
      </a>
    </div>
  </div>
</section>
