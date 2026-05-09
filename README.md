<p align="center">
<img width="320" height="280" alt="Image" src="https://github.com/user-attachments/assets/24911319-2e24-4cd2-a8ca-d6b905e770f7" />
</p>

# 📞 An Open CDR Standard

**An open, vendor-neutral schema for Call Detail Records - built by the industry, for the industry.**

---

## The Problem

Call Detail Records (CDRs) are fundamental to how telephony systems log, audit, and report on interactions. Yet despite being a near-universal concept across every platform and vendor, there is no shared, open standard for how CDR data is structured or exposed.

This creates real, tangible problems:

- **Vendor lock-in** — CDR formats are proprietary. Switching platforms or integrating across systems requires bespoke development work every time.
- **Specialist tooling required** — Accessing and making use of CDR data typically means purchasing expensive vendor-specific software or engaging specialist developers. Neither is accessible to smaller businesses.
- **Limited observability at scale** — Organisations running multi-vendor environments have no consistent way to correlate, audit, or analyse CDR data across their estate without significant investment.
- **Small businesses left behind** — The cost and complexity of CDR tooling means meaningful call observability is largely out of reach for small and medium-sized businesses, despite them having the same compliance, audit, and operational needs.

A common, open schema changes all of this. With a shared standard, any developer can build tooling, any business can consume CDR data without vendor dependency, and the entire industry benefits from a richer, more interoperable ecosystem.

---

## Project Goals

This project aims to establish a **prototype open standard** for CDR data, and to grow it into a fully realised, industry-backed specification.

### Phase 1 — Prototype *(current)*
- Define a comprehensive, vendor-neutral CDR field schema covering voice, video, chat, Meeitng, and multi-party interaction scenarios
- Publish a machine-readable OpenAPI 3.1 schema (`cdr-schema.yaml`)
- Publish human-readable field definitions and API guidelines
- Provide real-world example CDR responses covering common call scenarios
- Make all artefacts freely available under an open licence

### Phase 2 — Industry Sponsorship
- Engage telephony vendors, UC platform providers, call recording specialists, and compliance professionals to review and contribute to the schema
- Seek formal sponsorship and endorsement from industry bodies and working groups
- Establish a governance model for community-driven evolution of the standard

### Phase 3 — Realised Open Standard
- Publish a versioned, stable v1.0 specification with formal industry backing
- Build an active contributor community of industry professionals
- Establish a process for submitting, reviewing, and ratifying schema changes
- Encourage native adoption by switch vendors and platform providers as a standard API output

---

## Who We Are

This project was started by an industry professional with hands-on experience across **telephony, call recording, and call recording compliance** - someone who has seen first-hand the friction caused by the absence of a shared CDR standard.

Having worked across platforms, vendors, and compliance frameworks, the motivation here is straightforward: the industry deserves better interoperability, and the tooling gap particularly for smaller organisations is solvable with an open, collaborative approach.

This is not a commercial project. There is no product to sell. The goal is simply to put something useful into the world and invite others who care about the problem to help shape it.

---

## Repository Contents

| File | Description |
|------|-------------|
| `cdr-schema.yaml` | OpenAPI 3.1 machine-readable CDR schema |
| `CDR_Field_Definitions_v1.0.0.pdf` | Human-readable field definitions and API guidelines |
| `cdr-examples.json` | Example CDR API responses for five common call scenarios |

### Example Scenarios Covered

- **Inbound Call** - Simple two-party direct inbound voice call
- **Inbound Queue Call (IVR/ACD)** - Caller routed through IVR and ACD queue to agent
- **Outbound Call** - Agent-initiated outbound call
- **Inbound Call with Conference** - Agent adds a third-party specialist mid-call
- **Inbound Call with Transfer** - Warm transfer between agents, with both legs documented

---

## Schema Highlights

- **Vendor-neutral** - No proprietary fields, no platform-specific assumptions
- **Multi-party native** - Conferences, transfers, barge-in, and silent monitoring are first-class concepts
- **Full event timeline** - Every call carries an ordered `events` array capturing ringing, hold, transfer, IVR, queue, recording actions, and more
- **Modality-aware** - Voice, video, chat, instant message, and email interactions are all in scope
- **Extensible** - A `vendorSpecificFields` object allows platforms to include proprietary metadata without polluting the core schema
- **Pagination & filtering built in** — Time range, media type, group filtering, and consistent ordering are part of the API design from the start

---

## Get Involved

This standard only becomes meaningful with industry participation. Whether you are a switch vendor, a UC platform developer, a compliance specialist, a call recording integrator, or simply someone who has felt the pain of proprietary CDR formats - your input is welcome.

Ways to contribute:

- **Review the schema** - Does it cover your platform's data? What is missing? What should be different?
- **Raise issues** - Open an issue to flag gaps, ambiguities, or proposed additions
- **Submit a pull request** - Propose changes to the schema, field definitions, or examples
- **Spread the word** - Share this project with colleagues and organisations who would benefit from a common CDR standard

---

## Possible Future Areas of Expansion 

- A proper website/domain registration for the project
- A sister project for an Open CTI messaging standard 
- A Open call logging platform for ingesting CDR data written to the specification defined in this project.

---

## Licence

All artefacts in this repository are published under the **Apache 2.0 Licence** - free to use, free to build on, with no strings attached.

---

## Status

> 🟡 **Prototype** - The schema is complete and internally consistent. It is not yet formally endorsed by any industry body. Feedback, review, and contribution from industry professionals is actively sought.


