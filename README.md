# Biobeat (biobeat)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Biobeat Technologies Ltd. is an Israeli med-tech company (founded 2016, Petah Tikva) whose remote patient monitoring (RPM) health-AI platform pairs a disposable short-term **chest-monitor** and a reusable long-term **wrist-monitor** - both built on a photoplethysmography (PPG) sensor - to continuously track up to 13 vital signs. Biobeat's wearables were the first FDA-cleared devices for cuffless, non-invasive, PPG-based blood pressure monitoring, and are also CE Mark certified. Readings stream to Biobeat's HIPAA- and GDPR-compliant, cloud-based patient management platform, where clinicians view real-time data, trends, and configurable alerts across many patients at once.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/biobeat/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/biobeat/refs/heads/main/apis.yml)

## Access Model - Please Read

**Biobeat does not publish a self-serve public developer API.** There is no developer portal, no public API reference, no OpenAPI, and no published base URL or authentication scheme.

What is real and documented in public materials:

- Biobeat offers programmatic data access as a **paid add-on**. Multiple public sources describe an "API add-on" that lets a customer **download raw measurement data** for maintaining clinical histories and for research.
- Patient data can **sync into a hospital EMR/EHR system**. Public materials note the raw export is not immediately turnkey - a health service needs its own programming/analytics resources (or a partner) to build interfaces into their EMR.
- The clinician-facing platform is delivered as regional cloud tenants (for example `remote-monitoring.us.bio-beat.cloud` and `remote-monitoring.eu.bio-beat.cloud`), behind authenticated login.
- Biobeat data also reaches care teams through **integration partners** rather than a direct public API - e.g. Current Health (Best Buy Health), Datos Health, and Impilo.

Because access is partner-gated, the API entries in `apis.yml` are **logical, modeled resources** (Patients, Devices, Vital Signs Measurements, Alerts) inferred from Biobeat's public product descriptions. Endpoint paths, the `api.us.bio-beat.cloud` base URL, request/response shapes, and auth are **modeled, not confirmed** - do not treat them as a contract. To obtain real API access, credentials, and documentation, contact Biobeat directly.

## Tags

- Remote Patient Monitoring
- RPM
- Wearables
- Vital Signs
- Cuffless Blood Pressure
- Digital Health
- Medical Devices
- PPG
- Partner Gated

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

### Biobeat Patients API

Modeled resource for enrolling and managing monitored patients on the Biobeat patient management platform - create, list, and update patient records, assign devices, and set per-patient alarm limits. Endpoints are modeled; access is a partner-gated paid add-on.

- **Human URL:** [https://www.bio-beat.com/](https://www.bio-beat.com/)
- **Base URL (modeled):** `https://api.us.bio-beat.cloud`

### Biobeat Devices API

Modeled resource for provisioning and managing Biobeat wearable devices - the disposable chest-monitor and the reusable wrist-monitor - including registration, patient assignment, and status/battery lifecycle. Endpoints are modeled.

- **Human URL:** [https://www.bio-beat.com/](https://www.bio-beat.com/)
- **Base URL (modeled):** `https://api.us.bio-beat.cloud`

### Biobeat Vital Signs Measurements API

Modeled resource for retrieving continuous vital-sign readings - cuffless blood pressure, pulse rate, respiratory rate, blood oxygen saturation, temperature, stroke volume, cardiac output, and one-lead ECG. Maps to Biobeat's documented "API add-on" for downloading raw measurement data, delivered under a partner agreement.

- **Human URL:** [https://www.bio-beat.com/](https://www.bio-beat.com/)
- **Base URL (modeled):** `https://api.us.bio-beat.cloud`

### Biobeat Alerts API

Modeled resource for the alerts Biobeat raises when readings cross configured alarm limits or its health-AI flags early deterioration - listing active alerts and per-patient threshold configuration. Endpoints are modeled; alerts are surfaced in Biobeat's clinician dashboard.

- **Human URL:** [https://www.bio-beat.com/](https://www.bio-beat.com/)
- **Base URL (modeled):** `https://api.us.bio-beat.cloud`

## Common Properties

- [LinkedIn](https://il.linkedin.com/company/biobeat-ltd.)
- [Website](https://www.bio-beat.com/)
- [Portal](https://remote-monitoring.us.bio-beat.cloud/)
- [Plans](plans/biobeat-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
