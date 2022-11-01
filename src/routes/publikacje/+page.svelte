<script>
  const base = "https://wydawnictwo.horyzont.eu/publikacje/";

  const team = [
    ["Piotr Kardasz", "Redaktor Naczelny", "Editor-in-Chief"],
    ["Mirosław Dela", "Z-ca Redaktora Naczelnego", "Deputy Editor-in-Chief"],
    ["Łukasz Jeleń", "Redaktor Merytoryczny", "Content Editor"],
    ["Ryszarda Getko", "Redaktor Statystyczny", "Statistics Editor"],
    ["Jakub Zbądzki", "Redaktor Językowy", "Language Editor"],
    ["Marcin Radzewicz", "Sekretarz Redakcji", "Assistant Editor"],
  ];

  const tabs = [
    "Aktualny numer",
    "Turystyka i Rekreacja",
    "Informatyka",
    "Filologia",
  ];

  const publications = [
    [],
    [
      ["2010 1(1)", "", "", "Turystyka/art.pdf"],
      ["2011 2(2)", "", "", "Turystyka/biuletynTiRnr2.pdf"],
      ["2012 3(3)", "", "", "Turystyka/TiR2012.pdf"],
    ],
    [
      [
        "2011 1",
        "Informatyka/Spis_tresci_1_2011.pdf",
        "Informatyka/streszczenie_nr_1_2011.pdf",
        "Informatyka/biuletynInfnr1.pdf",
        [
          {
            text: "Errata",
            href: "https://wydawnictwo.horyzont.eu/publikacje/Informatyka/ErrataInf_1_2011.pdf",
          },
        ],
      ],
      [
        "2012 2",
        "Informatyka/Spis_tresci_2_2012.pdf",
        "Informatyka/streszczenia_nr_2_2012.pdf",
        "Informatyka/biuletynInfnr2.pdf",
      ],
      [
        "2013 3",
        "Informatyka/Spis_tresci_3_2013.pdf",
        "Informatyka/streszczenia_nr_3_2013.pdf",
        "Informatyka/biuletynInfnr3.pdf",
        [
          {
            text: "C. Koscielny, Aplikacje c80k395.mw",
            href: "https://wydawnictwo.horyzont.eu/publikacje/Informatyka/c80k395.mw",
          },
          {
            text: "C. Koscielny, Aplikacje c80k395mp.mw",
            href: "https://wydawnictwo.horyzont.eu/publikacje/Informatyka/c80k395mp.mw",
          },
        ],
      ],
      [
        "2014 4",
        "Informatyka/Spis_tresci_4_2014.pdf",
        "Informatyka/streszczenia_nr_4_2014.pdf",
        "Informatyka/biuletynInfnr4.pdf",
      ],
      [
        "2015 5",
        "Informatyka/Spis_tresci_5_2015.pdf",
        "Informatyka/streszczenia_nr_5_2015.pdf",
        "Informatyka/biuletynInfnr5.pdf",
      ],
      [
        "2016 6",
        "Informatyka/Spis_tresci_6_2016.pdf",
        "",
        "Informatyka/biuletynInfnr6.pdf",
        [
          {
            text: "C. Koscielny, Aplikacja a256k8192.mw",
            href: "https://wydawnictwo.horyzont.eu/publikacje/Informatyka/a256k8192.mw",
          },
        ],
      ],
      [
        "2017 7-1",
        "Informatyka/Spis_tresci_7-1_2017.pdf",
        "Informatyka/streszczenia_nr_7-1_2017.pdf",
        "Informatyka/biuletynInfnr7-1.pdf",
      ],
      [
        "2017 7-2",
        "Informatyka/Spis_tresci_7-2_2017.pdf",
        "Informatyka/streszczenia_nr_7-2_2017.pdf",
        "Informatyka/biuletynInfnr7-2.pdf",
      ],
      [
        "2018 8",
        "Informatyka/Spis_tresci_8_2018.pdf",
        "Informatyka/streszczenia_nr_8_2018.pdf",
        "Informatyka/biuletynInfnr8.pdf",
      ],
      [
        "2022 9",
        "Informatyka/Spis_tresci_9_2022.pdf",
        "Informatyka/streszczenia_nr_9_2022.pdf",
        "Informatyka/biuletynInfnr9.pdf",
      ],
    ],
    [["2011 1(1)", "", "", "Filologia/biuletynFilnr1.pdf"]],
  ];

  const paperSeries = [
    "2011 1",
    "2012 2",
    "2013 3",
    "2014 4",
    "2015 5",
    "2016 6",
    "2017 7-1",
    "2017 7-2",
    "2018 8",
    "2022 9",
  ];

  const steps = [
    [
      "Wskazówki",
      "https://wydawnictwo.horyzont.eu/publikacje/wskazowki/Informatyka.pdf",
    ],
    [
      "Zasady etyczne",
      "https://wydawnictwo.horyzont.eu/publikacje/wskazowki/Zasady_etyczne.pdf",
    ],
    [
      "Wzór umowy zawieranej z autorami - CC BY 4.0",
      "https://wydawnictwo.horyzont.eu/publikacje/wskazowki/Wzor_umowy-CC_BY_4_0.pdf",
    ],
    ["Kontakt", "mailto:wydawnictwo@horyzont.eu"],
  ];

  let tabIndex = 1;

  function getLinkText(i) {
    if (i == 1) return "Spis treści";
    if (i == 2) return "Streszczenia";
    if (i == 3) return "Pełne teksty";
  }

  function changePublicationType(i) {
    tabIndex = i;
  }

  function calculateStepColor(i) {
    if (i == 0) return "bg-green-50";
    if (i == 1) return "bg-green-100";
    if (i == 2) return "bg-green-200";
    if (i == 3) return "bg-green-300";
  }
</script>

<!-- TODO: Aktualny numer -->

<main class="flex flex-col py-20 items-center gap-96">
  <section class="w-1/2">
    <h1 class="text-6xl font-bold pb-8">Redakcje Czasopisma</h1>
    <div class="grid grid-cols-3 gap-20">
      {#each team as t}
        <div class="card lg:card-side bg-base-100 shadow-xl w-64">
          <div class="card-body flex flex-col items-center text-center">
            <div class="avatar">
              <div class="w-24 rounded-full">
                <img src="https://placeimg.com/192/192/people" />
              </div>
            </div>
            <h2 class="card-title ">{t[0]}</h2>
            <p>{t[1]}</p>
            <p>{t[2]}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>
  <section class="w-1/2">
    <h1 class="text-6xl font-bold pb-8">Dla autorów</h1>
    <ul class="steps steps-vertical">
      {#each steps as step, i}
        {@const color = calculateStepColor(i)}
        <li class="step step-neutral">
          <div class="alert {color} shadow-lg">
            <div>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="w-6 h-6"
              >
                {#if i < 2}
                  <path
                    d="M11.25 4.533A9.707 9.707 0 006 3a9.735 9.735 0 00-3.25.555.75.75 0 00-.5.707v14.25a.75.75 0 001 .707A8.237 8.237 0 016 18.75c1.995 0 3.823.707 5.25 1.886V4.533zM12.75 20.636A8.214 8.214 0 0118 18.75c.966 0 1.89.166 2.75.47a.75.75 0 001-.708V4.262a.75.75 0 00-.5-.707A9.735 9.735 0 0018 3a9.707 9.707 0 00-5.25 1.533v16.103z"
                  />
                {:else if i == 2}
                  <path
                    d="M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-12.15 12.15a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32L19.513 8.2z"
                  />
                {:else}
                  <path
                    d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.928 5.493a3 3 0 01-3.144 0L1.5 8.67z"
                  />
                  <path
                    d="M22.5 6.908V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.158l9.714 5.978a1.5 1.5 0 001.572 0L22.5 6.908z"
                  />
                {/if}
              </svg>
              <a href={step[1]} target="_blank">{step[0]}</a>
            </div>
          </div>
        </li>
      {/each}
    </ul>
  </section>
  <section class="w-1/2">
    <h1 class="text-6xl font-bold pb-8">Publikacje</h1>
    <div class="tabs pb-4">
      {#each tabs as tab, i}
        <button
          on:click={() => changePublicationType(i)}
          class="tab text-xl {i == tabIndex ? 'tab-active' : ''}"
        >
          {tab}
        </button>
      {/each}
    </div>
    <div class=" gap-2 relative">
      <div class="absolute stack w-96 -rotate-6 -z-10 -left-96 top-8">
        <div class="card shadow-md bg-yellow-50 text-primary-content">
          <div class="card-body">
            <h2 class="card-title">Deklaracja o wersji pierwotnej</h2>
            <p>
              Wersją pierwotną Biuletynu Naukowego Wrocławskiej Wyższej Szkoły
              Informatyki Stosowanej. Informatyka,
            </p>
            {#each paperSeries as serie}
              <p>{serie},</p>
            {/each}
            <p>
              Wersją pierwotną Biuletynu Naukowego Wrocławskiej Wyższej Szkoły
              Informatyki Stosowanej. Turystyka i Rekreacja,
            </p>
            <p>2011 2(2)</p>
            <p>2012 3(3)</p>
            <p>jest wydanie papierowe.</p>
          </div>
        </div>
        {#each { length: 3 } as _}
          <div class="card shadow bg-yellow-50 text-primary-content">
            <div class="card-body" />
          </div>
        {/each}
      </div>
      <div class="grid grid-cols-2 gap-4">
        {#each publications[tabIndex] as p}
          <div class="alert shadow-lg flex-col items-start ">
            <div class="flex flex-row justify-between">
              <h3 class="font-bold">
                Biuletyn Naukowy Wrocławskiej Wyższej Szkoły Informatyki
                Stosowanej. {tabs[tabIndex]}, {p[0]}
              </h3>
              <div class="flex flex-col">
                {#each p as href, i}
                  {#if i != 0 && i != 4}
                    {@const linkText = getLinkText(i)}
                    <button disabled={href == ""} class="btn btn-sm w-32 my-1"
                      ><a target="_blank" href={base + href}>{linkText}</a>
                    </button>
                  {/if}
                {/each}
              </div>
            </div>
            {#if p.length == 5}
              {#each p[4] as { text, href }}
                <a class="link link-secondary" target="_blank" {href}>{text}</a>
              {/each}
              <!-- <a href="" /> -->
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </section>
</main>
