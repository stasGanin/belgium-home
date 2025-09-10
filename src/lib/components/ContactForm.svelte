<script>
  import { Mail, Phone } from "lucide-svelte";
</script>

<section id="contact" class="py-16">
  <div class="max-w-3xl mx-auto px-4 text-center">
    <h2 class="text-3xl font-bold mb-6">Neem contact met ons op</h2>
    <p class="mb-8 text-gray-600">
      Laat een bericht achter of neem rechtstreeks contact op:
    </p>

    <div class="flex flex-col gap-4 items-center">
      <a
        href="tel:+32477935991"
        class="flex items-center gap-2 px-6 py-3 bg-blue-600 text-white rounded-xl shadow hover:bg-blue-700 transition"
      >
        <Phone size={20} /> 0477 93 59 91
      </a>
      <a
        href="mailto:igor.ganin@gmail.com"
        class="flex items-center gap-2 px-6 py-3 bg-gray-800 text-white rounded-xl shadow hover:bg-gray-900 transition"
      >
        <Mail size={20} /> igor.ganin@gmail.com
      </a>
    </div>
  </div>
</section>
