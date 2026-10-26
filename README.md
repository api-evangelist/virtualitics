# Virtualitics

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Virtualitics, Inc. is a Pasadena, California AI software company founded in 2016 on more than a decade
of research at Caltech and NASA's Jet Propulsion Laboratory. It builds the Virtualitics AI Platform
(VAIP), Virtualitics Explore, Virtualitics Predict, the Integrated Readiness Optimization (IRO)
application suite, and Iris — a natural-language agent over platform data — largely for U.S. defense,
government and critical-infrastructure customers.

Its developer surface is **Python-first, not HTTP-first**. There is no published OpenAPI, GraphQL,
AsyncAPI, gRPC or SOAP contract on any Virtualitics host. What the company does publish is a real and
maintained programming contract:

- **Virtualitics SDK** (`virtualitics-sdk` on PyPI) — the framework for authoring AI Apps, with a
  versioned documentation site at <https://sdk.virtualitics.com/latest/> and a migration guide that
  records breaking changes per minor version.
- **Virtualitics CLI** (`virtualitics-cli`, the `vaip` command) — the only published path for
  packaging and deploying an App into a customer tenant.
- **pyVIP** (`pyvip`) — the Python API that drives Virtualitics Explore over a WebSocket.

### Notable findings from the 2026-09-04 profiling pass

- **`api.virtualitics.com` no longer resolves.** It is the only project URL pyVIP publishes on PyPI
  and the host every search result points at for the pyVIP API reference. NXDOMAIN from both 8.8.8.8
  and 1.1.1.1. The package is still maintained (1.27.1, 2026-02-11); its reference documentation is
  not reachable.
- **The vulnerability reporting policy is at the wrong URL.**
  <https://virtualitics.com/vulnerability-reporting-policy/> returns 200 with that title and serves
  the Terms of Use. The real policy — with safe harbor, a 90-day disclosure window and a
  `security@virtualitics.com` channel — lives at <https://virtualitics.com/disclosures/>.
- **No `security.txt`** on any host, despite a genuine disclosure program existing.
- **No pricing page.** `/pricing/` returns a soft-200 serving the homepage and is absent from the
  site's own sitemap; the motion is contact-sales.
- **No `/.well-known/` documents** anywhere. `accounts.virtualitics.com` answers 200 for every
  extension-less path with the same 8,134-byte SPA shell — a negative control confirms those 200s
  are catch-alls, not documents.

See `apis.yml` for the full artifact index.
