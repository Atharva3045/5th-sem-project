# 🌸 Vyana Care 

**A voice-first, offline-resilient maternal healthcare platform for rural India.**

> **Project status:** Week 1 — planning and development from scratch. Features described below are planned unless explicitly marked as implemented.

## Overview

Vyana Care aims to make essential pregnancy guidance easier to access for women in rural and low-connectivity communities. The project focuses on simple Hindi-first interactions, recognition of pregnancy warning signs, and coordination with ASHA workers.

**Development strategy:** Start with a mobile-friendly web application, progressively add installable/offline PWA functionality, and develop a dedicated Android application in a future phase.

## The Problem

- **Language and literacy barriers:** Many patients find medical terminology and text-heavy apps difficult to use.
- **Unreliable connectivity:** Internet access may be slow, intermittent, or unavailable.
- **Delayed escalation:** Important pregnancy warning signs may not reach a healthcare professional quickly.
- **Frontline workload:** ASHA workers need practical tools for prioritizing follow-ups.

## Planned Features

### Phase 1 — Web App (initial release)
- Mobile-friendly patient interface
- Hindi and English language options
- Pregnancy education and safety information
- Symptom reporting with predefined, clinically reviewed warning-sign rules
- Clear emergency guidance and calling options
- Basic ASHA worker view for reviewing reports
- Accessible interface designed for low-literacy users

### Phase 2 — AI, Voice, and Offline PWA
- Voice-based interaction for supported languages
- AI-assisted information and symptom intake, with safety safeguards
- Offline access to previously downloaded guidance and warning-sign instructions
- Secure synchronization of non-emergency records when connectivity returns
- Telephone-based voice assistant for callers with cellular voice service
- Consent-based alerts and ASHA follow-up workflows

### Phase 3 — Android App (future)
- Native Android experience with stronger device integrations
- Experimental Bluetooth-based relay of small encrypted SOS messages between **participating, consenting devices**
- Store-and-forward delivery through an internet-connected relay, where available

**Important:** Bluetooth relay is a research/development goal, not a guaranteed emergency channel. Without cellular or internet access, emergency calls and server notifications cannot be assumed to work. The app must clearly distinguish *message queued*, *message delivered*, and *help confirmed*.

## How Vyana Care Is Intended to Work

1. A user opens Vyana Care and selects a language.
2. She reads or listens to pregnancy guidance and may report symptoms.
3. A safety-focused rules system checks for predefined warning signs.
4. Serious warning signs prompt immediate medical-care guidance, not a diagnosis.
5. When connectivity and consent permit, the system may help contact an ASHA worker or emergency service.
6. Selected guidance remains accessible offline after it has been downloaded.

**Medical safety:** Vyana Care is intended as a support tool, not a replacement for clinicians, diagnosis, or emergency services. Clinical content and escalation rules require qualified medical review before real-world use.

## Proposed Technology Stack

| Area | Planned technology |
| --- | --- |
| Web frontend | HTML, CSS, JavaScript; React + Vite as the app grows |
| Backend API | Python + FastAPI |
| Database | SQLite for development; PostgreSQL when appropriate |
| Offline web support | Progressive Web App (PWA), service workers, local storage |
| AI services | To be selected and evaluated for safety, language support, and cost |
| Voice output | ElevenLabs or another suitable speech provider (planned) |
| Future Android app | Kotlin + Jetpack Compose |
| Future nearby relay | Android Bluetooth APIs (experimental) |

The frontend and future Android app are intended to share a backend API.

## Week 1 — Development Plan

- **Day 1:** Set up VS Code, Git, Node.js, and Python; initialize the repository.
- **Day 2:** Create a responsive homepage using HTML and CSS.
- **Day 3:** Add basic JavaScript interactions, language selection, and forms.
- **Day 4:** Set up React and reusable UI components.
- **Day 5:** Create a minimal FastAPI backend and connect it to the frontend.
- **Day 6:** Prototype a safety-focused symptom reporting form using predefined rules.
- **Day 7:** Test on desktop and mobile; review accessibility and next steps.

**Week 1 goal:** A working local prototype with a homepage, navigation, and basic symptom-reporting interface. No production medical claims or live emergency dispatch.

## Proposed Repository Structure

```text
vyana-care/
├── README.md
├── frontend/          # Web app (React / Vite)
├── backend/           # FastAPI services
├── docs/              # Product, safety, and architecture notes
└── tests/             # Automated tests (added as features grow)
```

Folders will be created as development progresses.

## Local Setup

Development setup instructions will be added once the first working frontend and backend are created. This repository is currently at the initial planning stage.

## Privacy and Responsible Development

- Obtain informed consent before collecting personal or health information.
- Minimize and protect sensitive data; never commit credentials to GitHub.
- Apply appropriate access controls and encryption.
- Review applicable Indian data-protection requirements before deployment.
- Test emergency workflows carefully; never imply an alert has been received without confirmation.

## Roadmap

- [ ] Initialize project and repository
- [ ] Build responsive homepage
- [ ] Add Hindi/English interface
- [ ] Create symptom-reporting prototype
- [ ] Connect frontend to FastAPI
- [ ] Add reviewed pregnancy guidance
- [ ] Implement offline PWA features
- [ ] Prototype ASHA dashboard
- [ ] Explore voice and telephone integration
- [ ] Plan Android application
- [ ] Research Bluetooth emergency relay



## License

A license has not yet been selected for this new implementation.
