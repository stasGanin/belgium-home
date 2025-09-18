<script>
  import { ChevronDown, ChevronUp } from "lucide-svelte";

  const specs = [
    
    {
      title: "Vloeren & Wanden",
      content: `
- Doorlopende gepolierde keramische tegelvloeren in alle leefruimtes (living, keuken, slaapkamers, inkomhal, berging, nachthal).
- Toiletten en badkamers: vloeren in harmonie met de wandtegels.
- Keuken: wandafwerking in lichtgekleurd glas (onderhoudsvriendelijk en hygiënisch).
- Venstertabletten: graniet in living en keuken, marmer in slaapkamers.
- Plafonds en muren: traditioneel gepleisterd.
      `
    },
    {
      title: "Deuren",
      content: `
- Inkomdeuren: brandwerend, wit gelakt, anti-inbraaksluiting, cilinderslot en inox krukken.
- Binnendeuren: wit gelakt, geprofileerd, met onzichtbare bevestiging, voorzien van slot en inox krukken.
- Speciale deur living–hal: glazen deur in gelaagd glas met zandstraaleffect, inox trekkers en ingebouwde vloerdranger.
- Kelders: schilderdeuren met cilinderslot en inox kruk.
      `
    },
    {
      title: "Elektriciteit & Verlichting",
      content: `
- Groot aantal stopcontacten en lichtpunten, optimaal verspreid per ruimte.
- Aansluitingen voor kabel-tv, telefoon en internet in living en slaapkamers.
- Inbouwspots in inkomhal, living, keuken, badkamer en minstens één slaapkamer (vochtbestendig in de badkamer).
- Extra verlichting: TL-armatuur onder keukenkasten, spots in de dampkap en spiegelkasten, wandarmatuur op terras.
- Videofoon-parlofoon combinatie in de living.
- Individuele elektriciteitsmeter (dubbel tarief), moderne zekeringskast met automatische zekeringen en verliesstroomschakelaars.
- Private kelder voorzien van stopcontact en TL-verlichting, aangesloten op de eigen meter.
      `
    },
    {
      title: "Sanitair & Badkamer",
      content: `
- Toilet: san-bloc hangmodel met spaarknop, handwasbakje en toebehoren.

Badkamer:
- Ligbad in witte acryl, milieuvriendelijke 8-vorm (comfort met lager waterverbruik).
- Douche met glazen deur, drie betegelde wanden, ééngreepsmengkraan en verstelbare sproeikop.
- Dubbele lavabo’s in wit porselein, ingewerkt in een granieten blad met hoogglans onderkast.
- Spiegelkast met drie deuren en luifel met drie inbouwspots.
- Sierradiator met handdoekdroger.

Berging:
- Aansluiting voor wasmachine en condensdroogkast
- Uitgietbak met warm/koud water, mengkraan, handdoekhouder en zeepschaal
- Terras: voorzien van een vorstvrije waterkraan.

Alle toevoerleidingen warm/koud water in één stuk (geen koppelingen onder de vloer).
      `
    },
    {
      title: "Verwarming",
      content: `
- Centrale verwarming op aardgas, met individuele meter.
- Hoogrendements-condensatieketel (wandmodel) met geïntegreerde boiler en gesloten circuit.
- Alle radiatoren voorzien van thermostatische kranen.
- Centrale thermostaat in de living.
- Sierradiator met handdoekdroger in de badkamer.
- Leidingen onder de vloer in één stuk, zonder koppelingen.
      `
    },
    {
      title: "Keuken",
      content: `
Een ruime, luxe keukeninstallatie met hoogwaardige materialen en Siemens-inbouwtoestellen:

- Fronten in hoogglanslak, inox handgrepen, soft-close laden en pottenwagens.
- Bestekindeling in laden, beschermde gootsteenkast met uittrekbare handdoekhouder en vuilnisemmertje.

Inbouwtoestellen Siemens:
- Dampkap (90 cm breed, afvoer naar buiten, met 2 spots)
- Keramische kookplaat
- Grote koelkast met vriesvak
- Vaatwasser
- Oven met grill (inox front)
- Microgolfoven (inox front)

Werkbladen in massief gepolierd graniet (3 cm dik).
Dubbele inox spoelbak met afdruipblad (merk Franke, krasvrij) en designmengkraan met uittrekbare flexibele kraankop.
      `
    },
    {
      title: "Garage",
      content: `
 • Traditionele, volledig gemetste constructie met buitenmuren in gevelsteen en binnenmuren in witte silicaatsteen.
 • Dakconstructie in glad betongewelf, met roofing en aluminium dakranden in groene kleur.
 • Hoogwaardige geïsoleerde sectionaalpoort van Crawford, elektrisch bediend (2 afstandsbedieningen inbegrepen).
 • Veiligheidssystemen: fotocelbeveiliging, ingebouwde verlichting, manuele vergrendeling, veiligheidsstootbanden.
 • Voorzien van eigen stopcontact, aparte motor-aansluiting en TL-armatuur.
 • Aangesloten op de individuele elektriciteitsmeter van het appartement.
      `
    }
  ];

  let openIndex = null;

  function toggle(index) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section id="specs" class="py-16 bg-gray-50">
  <h2 class="text-3xl font-bold text-center mb-10">Technische Details</h2>

  <div class="max-w-3xl mx-auto flex flex-col gap-6 px-4">
    {#each specs as spec, i}
      <div class="bg-white shadow-lg rounded-xl overflow-hidden transition">
        <button
          class="w-full flex justify-between items-center px-6 py-4 text-left font-semibold text-gray-800 hover:bg-gray-100 transition"
          on:click={() => toggle(i)}
        >
          <span>{spec.title}</span>
          {#if openIndex === i}
            <ChevronUp size={20} />
          {:else}
            <ChevronDown size={20} />
          {/if}
        </button>

        <div
          class="px-6 overflow-hidden transition-all duration-300"
          style="max-height: {openIndex === i ? '1000px' : '0'}"
        >
          <p class="py-4 text-gray-600 whitespace-pre-line">{spec.content}</p>
        </div>
      </div>
    {/each}
  </div>
</section>
