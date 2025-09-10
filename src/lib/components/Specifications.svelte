<script>
  import { ChevronDown, ChevronUp } from "lucide-svelte";

  const specs = [
    {
      title: "Garages",
      content: `
Volledig traditioneel gemetste konstruktie, buitenmuren gemetst in gevelsteen (idem hoofdgebouw), binnenmuren gemetst in witte silicaat-steen met zogenaamde “velkanten” (afgeschuinde kanten), mooi afgewerkt, hoeft niet geschilderd te worden;
vloer in gladde beton;
dakkonstruktie in gladde betongewelven (geen houten roostering), roofing-dakbedekking, afgewerkt met gemoffelde alu-dakranden in groene kleur;
hoogwaardige geïsoleerde sectionaal-poort Crawford, elektrisch bediend (2 afstandsbedieningen bijgeleverd), manuele vergrendelingsmogelijkheid, motor met ingebouwde verlichting, 2 kunststof-veiligheidsstootbanden aan de zijkanten van de poort, bedieningsknop voor de poort binnenin de garage, optische veiligheidsogen (fotocel-beveiliging) zodat de poort niet kan dichtgaan indien er zich iemand of iets onder de poort bevindt (uitrusting volledig conform nieuwe strenge Europese wetgeving die binnenkort van kracht wordt);
individueel vrij stopkontakt + apart stopkontakt voor motor van de poort;
individueel lichtpunt met TL-armatuur (2 lampen)
de elektriciteit van de garages wordt aangesloten op de individuele elektriciteitsmeter van het appartement waartoe de garage zal behoren;
      `
    },
    {
      title: "Buitenschrijnwerken",
      content: `
Ramen en buitendeuren in zeer stevige en hoogwaardige aluminium-profielen (zogenaamde “drie-kamer-profielen” wat condens en koude bruggen vermijdt en optimale isolatie garandeert, “cement-grijs”-kleur aan de buitenkant, wit aan de binnenkant, voorzien van driedubbele rubber-sluitingen), inox-krukken;
De schuiframen zijn voorzien van een blokkeringssysteem (anti-diefstal-lat);
de meeste ramen zijn van het type draai-kip (slaapkamers, keukens);
alle ramen en buitendeuren zijn voorzien van dubbele isolerende beglazing;
de ramen zijn op de voorgevel voorzien van speciaal extra-geluidsisolerende beglazing (zeer sterke reductie van het straatlawaai: vermindering van 35 decibel);
      `
    },
    {
      title: "Vloer- en muurbekledingen",
      content: `
Alle plaatsen binnenin de appartementen zijn voorzien van hoogwaardige keramische gepolierde tegelvloeren met aangepaste tegelplinten. Zelfde doorlopende vloeren in living, bureel, keuken, berging, inkomhall, slaapkamers, nachthall). Vloeren in toiletten en badkamers aangepast aan de wandtegels;
er zijn overal decoratieve inox-deurstoppen (met rubber-stootband) geplaatst op de vloeren;
plafonds en muren zijn traditioneel gepleisterd;
alle toiletten en badkamers zijn voorzien van hoogwaardige wandtegels (faïences), rondom rond op volle hoogte, met bijpassende “listel” (biestegel) en bijkomende decoratieve motieftegels;
in de keukens zijn de muren tussen de werkbladen en de hangkasten en ter hoogte van de gootstenen bekleed met decoratief, licht gekleurd glas (zeer onderhoudsvriendelijk en hygiënisch: geen voegen);
de venstertabletten in living en keuken zijn uitgevoerd in graniet, de venstertabletten in de andere plaatsen (slaapkamers) zijn uitgevoerd in marmer;
de bevloering in de kelders bestaat uit gladde beton;
de vloeren van de private zolders worden afgeleverd in effen cement-chappe;
      `
    },
    {
      title: "Binnenschrijnwerk",
      content: `
De inkomdeuren van de appartementen zijn decoratieve brandvrije deuren (wit gelakt), zelfde profiel als de binnendeuren, ingewerkt cylinderslot (in combinatie met cylinderslot van de sasdeur in de gemeenschappelijke inkom), anti-inbraak-veiligheidssluiting, inox-kruk aan de binnen- en buitenkant;
de binnendeuren van de appartementen zijn wit gelakte decoratieve deurbladen (geprofileerd) met aangepast wit gelakt kassement en omlijsting (geen zichtbare nagel- en boorgaten), binnendeurslot met sleutel, inox-kruk;
de deur tussen living en private hall is een volledig glazen deur (gelaagd glas, “zandstraal-effect”) met in de vloer ingewerkte pneumatische deurpomp (deurblad draait 180°), inox-deurtrekker langs beide kanten;
de deuren van de private kelders zijn schilderdeuren (vlak deurblad met houten kassement en omlijsting) voorzien van cylinderslot en inox-kruk;
      `
    },
    {
      title: "Elektriciteit",
      content: `
Groot aantal stopkontakten en lichtpunten (in verhouding tot de grootte van de plaatsen);
ieder appartement heeft diverse aansluitingspunten voor kabel-tv, telefoon en internet (in de living, bureel, minstens in één van de slaapkamers), aansluitingspunten voorzien van individuele bekabelingen (geen aftakkingen);
inkomhall, living, keuken, bureel, badkamer, minstens één slaapkamer voorzien van inbouwspots (de meeste richtbaar, in de badkamers speciale vochtbestendige spots) op laagspanning met transfo’s (transfo’s zijn centraal ingekast en dus steeds goed bereikbaar);
onder de hangkasten in de keuken is er een TL-verlichtingsarmatuur;
de dampkappen in de keukens zijn voorzien van drie inbouwspots;
de spiegelkasten in de badkamers zijn voorzien van een luifel met inbouwspots;
alle terrassen en balkons (voor- en achtergevel) voorzien van wand-verlichtingsarmatuur of inbouwspot(s’) in de dakoversteek;
videofoon-parlofoon combinatie (toestel geplaatst in de living), de duplex-appartementen beschikken over 2 video-schermen (één in de living op de eerste verdieping en één in de nachthall op de tweede verdieping);
alle appartementen voorzien van een individuele elektriciteitsmeter (dubbel-uurtarief, geplaatst in gemeenschappelijk tellerlokaal) en zekeringskast met automatische zekeringen en verliesstroomschakelaars (geplaatst in private bergingen);
de private kelders zijn voorzien van een individueel stopkontakt en individuele verlichting (TL-armatuur), aangesloten op de individuele electriciteitsmeter van het corresponderende appartement;
      `
    },
    {
      title: "Sanitair",
      content: `
Alle appartementen zijn voorzien van een toilet type san-bloc (hangmodel ingewerkt in de muur) met 2 drukknoppen (spaarknop), handwasbakje, alle toebehoren (spiegel, handddoekdrager, zeepschaal, papierrolhouder);
de badkamers op het gelijkvloers zijn voorzien van een ligbad in witte acrylplaat (met ééngreeps-mengkraan en handdouche) en een douche (met glazen deur, 3 zijden gemetst en volledig betegeld, één-greepsmengkraan met in de hoogte verstelbare sproeikop);
alle ligbaden zijn in 8-vorm (milieuvriendelijk): door de naar binnenkomende wanden heeft men hetzelfde comfort met minder waterverbruik;
alle appartementen hebben een badkamer voorzien van 2 ovale inbouwlavabo’s in wit porselein, ingewerkt in graniet-blad, met ééngreepsmengkraan, onderbouwkast in wit gelakte deuren (hoogglans-lak), uitschuifbare handdoekdrager, spiegelkast met drie deuren, luifel met drie inbouwspots;
aansluiting voor wasmachine in de berging (toevoer en afvoer);
aansluitingsmogelijkheid voor droogkast in de berging (met condens-opvang, geen rechtstreekse uitlaat naar buiten);
uitgietbak met warm- en koud water in de berging, mengkraan, handdoekdrager, zeepschaal;
alle appartementen beschikken op het terras aan de achtergevel over een individuele waterkraan (vorstvrij);
alle toevoer-waterleidingen (warm en koud water) onder de vloeren bestaan uit één stuk (geen koppelingen onder de vloer);
      `
    },
    {
      title: "Centrale verwarming",
      content: `
Centrale verwarming op aardgas (met individuele aardgasmeter in het gemeenschappelijk tellerlokaal);
hoog-rendements-condensatie-wandgasketel, gesloten circuit (externe luchttoevoer), met geïntegreerde boiler (continu warm water);
alle radiatoren voorzien van een thermostatische kraan;
centrale, instelbare thermostaat in de living, de duplex-appartementen hebben de mogelijkheid tot het plaatsen van een bijkomende thermostaat in de nachthall (aansluitingspunt en bekabeling aanwezig);
sierradiator met handdoekdrager op de badkamer;
alle toevoerleidingen onder de vloeren bestaan uit één stuk (geen koppelingen onder de vloeren);
      `
    },
    {
      title: "Keukeninstallatie",
      content: `
Zeer ruime, hoogwaardige kwaliteitsvolle luxe-keukeninstallatie;
fronten van de keukenkasten in hoog-glans lak, inox-deurtrekkers, sokkel met ingewerkte water-profiellijst, zelf-sluitende telescopische laden en pottenwagens (zogenaamde “soft-sluiting”), 2 schuiven met bestekverdeling, kast onder gootsteen voorzien van metalen bescherm-bodempaneel, uitschuifbare handdoekdrager en vuilnisemmertje;
elektrische inbouwtoestellen Siemens: telescopische dampkap (90 cm. breed, individuele afzuiging naar buiten) met drie inbouwspots, keramische kookplaat, grote frigo met ***vriesvak, vaatwas, oven met grill (inox-front), micro-golfoven (inox-front);
werkbladen in massief graniet (3 cm. dikte, gepolierd);
inox-spoeltafel met 2 spoelbakken en afdruipblad (krasvrije inox, merk Franke), design-ééngreepsmengkraan met uittrekbare kraankop (met flexibel);
      `
    }
  ];

  let openIndex = null;

  function toggle(index) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section id="specs" class="py-16 bg-gray-50">
  <h2 class="text-3xl font-bold text-center mb-10">Technische specificaties</h2>

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
