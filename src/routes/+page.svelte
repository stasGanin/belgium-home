<script>
  import Header from "$lib/components/Header.svelte";
  import Hero from "$lib/components/Hero.svelte";
  import Gallery from "$lib/components/Gallery.svelte";
  import Plan from "$lib/components/Plan.svelte";
  import Description from "$lib/components/Description.svelte";
  import ContactForm from "$lib/components/ContactForm.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import Specifications from "$lib/components/Specifications.svelte";
</script>

<Header />

<main >
  <Hero />
  <Specifications />
  <Gallery />
  <Plan />
  <Description />
  <ContactForm />
  <Footer />
</main>
