# Biobeat (biobeat)

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
