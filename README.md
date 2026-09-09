# Nritya Katha

> Preserving traditional dance, one movement at a time.

Nritya Katha is a website-first VR and AI platform for preserving, teaching, and exploring traditional dance. It combines an interactive cultural museum with a practice studio, structured movement records, and measurable movement feedback.

The project is designed to make cultural learning more accessible without requiring a VR headset. Desktop and mobile experiences are core modes; WebXR is an optional immersive layer.

## Current Prototype

The current prototype is a self-contained A-Frame scene in [`src/index.html`](src/index.html). It includes:

- A virtual museum hub with themed rooms
- A practice studio transition
- Hinged interactive gates that open before navigation
- Local marble, wall, and carpet textures
- A reference dancer loaded from a glTF sample model
- MediaPipe pose-tracking integration for future practice feedback
- Desktop cursor and WebXR controller interaction

The wider product plan includes a cultural explorer, movement archive, Ghost Guru comparison view, Rhythm Coach, Dance DNA, progress tracking, and practitioner verification workflows. These are described in [`doc/02_PRD.md`](doc/02_PRD.md).

## Run Locally

No build step is required for the current prototype.

1. Clone the repository.
2. Open [`src/index.html`](src/index.html) in a modern browser, or serve the repository with a local HTTP server.
3. Allow camera access when using the practice features.

For a local server, one option is:

```powershell
python -m http.server 8000 --directory src
```

Then open <http://localhost:8000>.

The prototype loads A-Frame, A-Frame Extras, MediaPipe, audio, and a glTF sample model from external URLs, so an internet connection is currently required for the complete experience.

## Product Vision

The learning loop is:

**Discover -> Understand -> Observe -> Practice -> Analyze -> Correct -> Repeat -> Preserve**

The long-term platform will represent dance as structured movement data rather than video alone. A Movement Record can contain joint positions, joint angles, timing, rhythm, sequence data, cultural context, contributor information, source, and verification status.

Planned modules include:

- **Cultural Explorer:** Browse traditions by region and context.
- **Virtual Cultural Museum:** Explore origins, forms, instruments, costumes, movements, stories, masters, and practice.
- **Digital Movement Archive:** Store queryable, structured movement records.
- **VR Dance Studio:** Practice with a virtual instructor and reference dancer.
- **Ghost Guru:** Compare measurable body-position differences with visual overlays.
- **Rhythm Coach:** Review beat alignment and timing consistency.
- **Dance DNA:** Track personal practice strengths and focus areas.

## Principles

- AI feedback describes measurable movement features such as joint angles, timing, posture, and position. It does not judge cultural correctness.
- Cultural content must be sourced and carry a visible verification status.
- Practitioner knowledge, consent, attribution, and takedown rights are required for recorded or published contributions.
- VR enhances the experience but must not be required for core learning workflows.
- Scoring weights are provisional and require validation with dance practitioners.

## Repository Guide

```text
doc/
  01_Research.md                 Research questions and cultural considerations
  02_PRD.md                      Product requirements and MVP scope
  03_Technical_Design_ARD.md     Architecture, data model, and AI pipeline
  04_Decisions.md                Product and technical decisions
  05_agents.md                   Guidance for coding agents
  06_Design.md                   UX, accessibility, and interaction design
  07_Roadmap.md                  Phased delivery plan
src/
  index.html                     Current A-Frame prototype
  assets/                        Local visual assets
```

## Roadmap

The planned delivery sequence is:

1. Research and practitioner consultation
2. UX and information architecture
3. Museum and studio 3D environments
4. Pose tracking and movement records
5. AI comparison and measurable feedback
6. Progress and Dance DNA dashboard
7. Technical, accessibility, and practitioner review
8. Deployment and monitoring

See [`doc/07_Roadmap.md`](doc/07_Roadmap.md) for phase exit criteria.

## Project Status

This repository is an early interactive prototype. The museum scene and browser/WebXR interaction are being developed before the full backend, verified content pipeline, movement archive, and production AI comparison system.

## License and Cultural Stewardship

No license has been selected yet. Cultural material, practitioner contributions, recordings, and movement data must not be treated as freely reusable by default. Any future public content workflow should document source, attribution, consent, usage restrictions, and verification status.
