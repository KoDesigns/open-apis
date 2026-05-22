# Collected Open APIs

A personal reference catalog of open APIs and open data standards worth integrating into projects. This repo does not reimplement or wrap these services — it collects official documentation, entry points, and links so you can find the right source quickly.

## Contents

| API / standard | Domain | Primary provider |
| --- | --- | --- |
| [DATEX II](#datex-ii) | Traffic & travel information exchange | DATEX II / CEN |
| [YR (MET Weather API)](#yr-met-weather-api) | Weather forecasts & meteorological data | Norwegian Meteorological Institute (MET) |
| [Ruter (via Entur)](#ruter-via-entur) | Public transport in Oslo & Akershus | Ruter → Entur |

---

## DATEX II

**What it is:** DATEX II is the European standard for exchanging traffic and travel information between systems — road operators, traffic centres, navigation services, and ITS applications. It covers situations (incidents, roadworks), measured/elaborated traffic data, parking, VMS, and more. Data is typically exchanged as XML or JSON using defined profiles rather than a single REST endpoint.

**Why it matters:** Relevant for road status, incidents, travel information, and interoperability with Norwegian road data (Statens vegvesen maintains DATEX II resources).

### Official resources

| Resource | URL | Description |
| --- | --- | --- |
| Documentation portal | [docs.datex2.eu](https://docs.datex2.eu/) | Main technical documentation, organized by support level (Basics → Expert) |
| Support levels overview | [docs.datex2.eu/levels/](https://docs.datex2.eu/levels/) | Choose the right documentation depth for your role |
| Recommended profiles | [docs.datex2.eu/recommended-profiles/](https://docs.datex2.eu/recommended-profiles/) | Standard DATEX II profiles for common use cases |
| Academy | [datex2.eu/academy/](https://datex2.eu/academy/) | Guides, learning material, and community-oriented introductions |
| CEN specifications | [datex2.eu/specifications/](https://datex2.eu/specifications/) | Overview of the multi-part CEN 16157 standard |
| DATEX II Webtool | [webtool.datex2.eu](https://webtool.datex2.eu/) | Profile creation, schema generation, and validation |
| Vegvesen webapp examples (v3.1) | [git.vegvesen.no — webapp-examples](https://git.vegvesen.no/projects/DATEX2/repos/datex2-spesifications/browse/3.1/webapp-examples) | Example implementations from Statens vegvesen (Norwegian Public Roads Administration) |

### How to use

- **Getting started (Basics):** [DATEX II — How is it used to support your services?](https://docs.datex2.eu/v3.1/level0user/servicesupport.html)
- **Using DATEX II (Level 1):** [Using DATEX II](https://docs.datex2.eu/v3.3/using)
- **Profiling guide:** [Profiling guide](https://docs.datex2.eu/v3.3/profiling/index.html)
- **JSON support:** [DATEX II supports JSON as well as XML](https://docs.datex2.eu/v3.3/json.html)

> **Note:** When exchanging privacy-affected data, comply with GDPR. See warnings on the [documentation portal](https://docs.datex2.eu/).

---

## YR (MET Weather API)

**What it is:** Open weather and meteorological data from MET Norway, exposed via `api.met.no`. The most widely used product is **Locationforecast** — global weather forecasts by latitude/longitude. Additional products include radar, text forecasts, air quality, Frost (observations), and embeddable widgets.

**Why it matters:** Free, high-quality weather data for Norway and worldwide. Requires proper client identification and caching — requests without a valid `User-Agent` are blocked.

### Official resources

| Resource | URL | Description |
| --- | --- | --- |
| Developer portal | [developer.yr.no](https://developer.yr.no/) | Overview of all API products and news |
| Documentation index | [developer.yr.no/doc/](https://developer.yr.no/doc/) | Guides, reference, and examples |
| Terms of Service | [developer.yr.no/doc/TermsOfService](https://developer.yr.no/doc/TermsOfService) | **Read first** — identification, rate limits, attribution |
| Locationforecast (Swagger) | [api.met.no/weatherapi/locationforecast/2.0/](https://api.met.no/weatherapi/locationforecast/2.0/) | Interactive API explorer |
| Forecast JSON format | [developer.yr.no/doc/ForecastJSON/](https://developer.yr.no/doc/ForecastJSON/) | Structure of forecast response payloads |
| Available widgets | [developer.yr.no/doc/guides/AvailableWidgets/](https://developer.yr.no/doc/guides/AvailableWidgets/) | Embeddable Yr widgets for websites |

### How to use

- **Getting started:** [Getting Started](https://developer.yr.no/doc/GettingStarted/)
- **Locationforecast step-by-step:** [Using Locationforecast — HowTO](https://developer.yr.no/doc/locationforecast/HowTO/)

> **Requirements:** Set a descriptive `User-Agent` header (app name + contact info). Respect `Expires` / `Last-Modified` headers and cache responses. Use HTTPS. Round coordinates to max 4 decimal places.

---

## Ruter (via Entur)

**What it is:** Ruter operates public transport in Oslo and Akershus (bus, tram, metro, ferry, rail). **Route and real-time data are no longer served from Ruter-owned APIs** — they are published through **Entur**, the national registry for Norwegian public transport. Ruter appears as codespace **`RUT`** in Entur's real-time feeds.

**Why it matters:** Any app showing Ruter departures, journey planning, or live vehicle positions should use Entur's APIs or open data exports — not legacy Ruter endpoints.

### Official resources

| Resource | URL | Description |
| --- | --- | --- |
| Entur Developer | [developer.entur.org](https://developer.entur.org/) | Main developer portal for all Norwegian PT data |
| National route dataset (NLOD) | [data.norge.no — Nasjonalt rutedatasett](https://data.norge.no/nb/datasets/f8327e57-60fa-440f-9ecd-a8765ca13ae6/nasjonalt-rutedatasett-for-kollektivtrafikk-i-norge) | Dataset description; lists all APIs and downloads |
| Journey Planner v3 (GraphQL) | [developer.entur.org — Journey Planner](https://developer.entur.org/pages-journeyplanner-journeyplanner/) | Point-to-point travel & departure boards — `POST https://api.entur.io/journey-planner/v3/graphql` |
| Real-time data (SIRI / GTFS-RT) | [developer.entur.org — Real-Time](https://developer.entur.org/pages-real-time-intro/) | Live updates; Ruter = **`RUT`** codespace |
| Geocoder API | [developer.entur.org — Geocoder](https://developer.entur.org/pages-geocoder-intro/) | Search stop places and addresses (needed before departure boards) |
| Stop Place Registry | [developer.entur.org — NSR](https://developer.entur.org/pages-nsr-nsr/) | National stop place register (GraphQL) |
| Timetable data (NeTEx) | [developer.entur.org — Timetable](https://developer.entur.org/pages-timetable-timetable/) | Daily NeTEx file exports |
| Entur API overview | [developer.entur.org — Overview](https://developer.entur.org/pages-intro-overview/) | Full list of APIs and open-source projects |

### How to use

- **Get started (departure board example):** [Get Started](https://developer.entur.org/pages-intro-getstarted/)
- **Journey Planner v3:** [Journey Planner documentation & GraphQL IDE](https://developer.entur.org/pages-journeyplanner-journeyplanner/)
- **Real-time API:** [Real-Time API documentation](https://developer.entur.org/pages-real-time-api/)
- **Geocoder API:** [Geocoder API documentation](https://developer.entur.org/pages-geocoder-api/)

> **Requirements:** Send an `ET-Client-Name` header on API requests (format: `"company-application"`). Unidentified clients may be rate-limited or blocked.

---

## Adding more APIs

This collection is intentionally small to start. Candidates for future entries: Statens vegvesen traffic data, Entur-adjacent mobility APIs, Frost, Kartverket, Brønnøysundregistrene, etc.

When adding an entry, include:

1. A short description of what the API provides
2. Official documentation URLs (not third-party wrappers)
3. A **How to use** link pointing to the provider's own guide — not a reimplementation here

---

## License

This catalog (README and repo metadata) is reference material only. Each API has its own terms — notably [MET Terms of Service](https://developer.yr.no/doc/TermsOfService) and [Entur NLOD licence](https://developer.entur.org/). Always check the provider before use in production.
