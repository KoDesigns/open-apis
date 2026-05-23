# Offentlige norske API-er

Samling av **offisielle, åpne API-er** fra norske etater og operatører. Primært norske kilder — kun lenker til dokumentasjon hos tilbyderen, ingen wrappers.

Klikk en tilbyder for å utvide.

<details>
<summary><strong>Kartverket</strong></summary>

| Tjeneste | Dokumentasjon | Slik bruker du |
| --- | --- | --- |
| API og data | [kartverket.no](https://kartverket.no/api-og-data) | [Bruke API-er (Geonorge)](https://www.geonorge.no/aktuelt/om-geonorge/slik-bruker-du-geonorge/bruke-tjenester-og-api-er/) |

</details>

<details>
<summary><strong>Ruter</strong> · via Entur</summary>

| Tjeneste | Dokumentasjon | Slik bruker du |
| --- | --- | --- |
| Kollektivdata | [developer.entur.org](https://developer.entur.org/) | [Kom i gang](https://developer.entur.org/pages-intro-getstarted/) |
| Avvik / SIRI-SX | `api.entur.io/realtime/v1/rest/sx` | [SIRI-SX (Entur)](https://developer.entur.org/pages-real-time-intro) |

Ruter-data går via Entur (`RUT` codespace).

</details>

<details>
<summary><strong>Vegvesen</strong></summary>

| Tjeneste | Dokumentasjon | Slik bruker du |
| --- | --- | --- |
| Åpne data | [vegvesen.no](https://www.vegvesen.no/fag/teknologi/apne-data/et-utvalg-apne-data/) | [Slik får du tilgang](https://www.vegvesen.no/fag/teknologi/apne-data/slik-far-du-tilgang-til-et-api/) |
| DATEX trafikk | [vegvesen.no — DATEX](https://www.vegvesen.no/fag/teknologi/apne-data/et-utvalg-apne-data/hva-er-datex/) | [Bestill tilgang](https://www.vegvesen.no/fag/teknologi/apne-data/et-utvalg-apne-data/hva-er-datex/bestille-tilgang-til-datex/) |
| DatexII | [docs.datex2.eu](https://docs.datex2.eu/) | [Using DATEX II](https://docs.datex2.eu/v3.3/using) |
| DatexII Academy | [datex2.eu/academy](https://datex2.eu/academy/) | — |
| DatexII examples | [git.vegvesen.no](https://git.vegvesen.no/projects/DATEX2/repos/datex2-spesifications/browse/3.1/webapp-examples) | — |

</details>

<details>
<summary><strong>YR</strong> · MET Norway</summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Vær (locationforecast compact) | `api.met.no/weatherapi/locationforecast/2.0/compact` | [developer.yr.no](https://developer.yr.no/) |
| Detaljert prognose / UV (locationforecast complete) | `api.met.no/weatherapi/locationforecast/2.0/complete` | [developer.yr.no](https://developer.yr.no/) |
| Farevarsler (MetAlerts) | `api.met.no/weatherapi/metalerts/2.0/current.json` | [api.met.no](https://api.met.no/) |
| Luftkvalitet | `api.met.no/weatherapi/airqualityforecast/0.1/` | [api.met.no](https://api.met.no/) |
| Soloppgang / solnedgang | `api.met.no/weatherapi/sunrise/3.0/sun` | [api.met.no](https://api.met.no/) |

</details>

<details>
<summary><strong>NAAF</strong> · pollenvarsel</summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Pollenvarsel | `pollenvarsel.naaf.no/charts/forecast` | [pollenvarsel.naaf.no](https://pollenvarsel.naaf.no/) |

</details>

<details>
<summary><strong>Hva koster strømmen</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Spotpriser per sone | `hvakosterstrommen.no/api/v1/prices/{YYYY}/{MM}-{DD}_{ZONE}.json` | [hvakosterstrommen.no/strompris-api](https://www.hvakosterstrommen.no/strompris-api) |

</details>

<details>
<summary><strong>Sporveien</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Anleggsstatus (HTML-scraping) | `sporveien.no/prosjekter-og-arbeid/<slug>/` | [sporveien.no](https://sporveien.no/) |

Ingen offentlig API — siden scrapes som HTML.

</details>

<details>
<summary><strong>Posten</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Postleveringsdager | `posten.no/.../delivery-days?postalCode=...` | [posten.no](https://www.posten.no/) |

</details>

<details>
<summary><strong>Oslo kommune</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Søppeltømming (REG) | `oslo.kommune.no/actions/snap-lib-waste-complaint/search-by-address` | [developer.oslo.kommune.no](https://developer.oslo.kommune.no/) |

</details>

<details>
<summary><strong>Vinmonopolet</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Butikk / åpningstider | `vinmonopolet.no/vmpws/v2/vmp/stores/{store_id}?fields=FULL` | [apent.vinmonopolet.no](https://apent.vinmonopolet.no/) |

</details>

<details>
<summary><strong>NRK</strong> · RSS</summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Oslo og Viken — siste | `nrk.no/osloogviken/siste.rss` | [nrk.no](https://www.nrk.no/) |
| Sport — toppsaker | `nrk.no/sport/toppsaker.rss` | [nrk.no](https://www.nrk.no/) |

</details>

<details>
<summary><strong>VG</strong> · RSS</summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Fotball (kategori 1066) | `vg.no/rss/feed/?format=rss&categories=1066` | [vg.no](https://www.vg.no/) |

</details>

<details>
<summary><strong>FIFA</strong></summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Kalender / kamper + livestatus | `api.fifa.com/api/v3/calendar/matches` | [fifa.com](https://www.fifa.com/) |

</details>

<details>
<summary><strong>Wikipedia</strong> · Wikimedia REST</summary>

| Tjeneste | Endepunkt | Dokumentasjon |
| --- | --- | --- |
| Sidens HTML (dagens dato) | `no.wikipedia.org/api/rest_v1/page/html/{day}._{month}` | [Wikimedia REST API](https://en.wikipedia.org/api/rest_v1/) |

</details>

Sjekk vilkår hos hver tilbyder før produksjonsbruk.

---

*English: Curated links to official open APIs from Norwegian public agencies and operators. Links only — no wrappers.*
