# NEXTEP (SDC Hackathon 2026 - Group SDC4)

> NEXTEP is an AI-driven, privacy-first career navigation platform designed to help Electrical and Electronic Engineering (EEE) students bridge academic gaps and transition smoothly into high-tech industry roles amidst rapid AI disruption.

---

## Team Information

| Field                  | Details                                     |
| ---------------------- | ------------------------------------------- |
| **Team Name**          | SDC4                                        |
| **Team Domain**        | Domain 1                                    |
| **SDG Track (1–17)**   | 4 (Quality Education), 8 (Decent Work and Economic Growth) |
| **Team Leader**        | YUE XIONGHE                                 |
| **University**         | XIAMEN UNIVERSITY MALAYSIA                  |
| **Number of Members**  | 4                                           |

## Links

| Resource          | Link                                           |
| ----------------- | ---------------------------------------------- |
| GitHub Repository | https://github.com/ERYCYUE/SDC_HACKATHON_SUBMISSION_TEMPLATE_GROUP_SDC4 |
| Replit Project    | https://nextep-ericyywies.replit.app           |
| Live Demo         | https://nextep-ericyywies.replit.app    |
| Slide Deck        | https://docs.google.com/presentation/d/1SvRvFLILOR-uoKKNbsVYxNxe0nVKZh4c/edit?usp=drive_link&ouid=101313800651987045018&rtpof=true&sd=true                     |
| Demo Video        | https://youtu.be/HySeHsjcdzk|

---

## Overview

### Problem

Graduating Electrical and Electronic Engineering (EEE) students face severe career anxiety and structural skill mismatch as emerging technologies outpace traditional academic curricula. Over 65% of students report uncertainty in their career trajectories, struggling to identify actionable transition pathways into high-demand tech and green engineering roles.

### Solution

NEXTEP harnesses Generative AI (DeepSeek API) and massive real-time recruitment analytics to transform market signals into personalized career guidance. By evaluating individual student profiles, the platform automatically generates step-by-step upskilling roadmaps while strictly safeguarding user privacy through a client-side architecture.

### Key Features

- **AI-Powered Skill Gap Analysis** — Automatically evaluates EEE student profiles against emerging industry demands.
- **Tailored Reskilling Roadmaps** — Generates customized, milestone-based learning paths to achieve long-term career goals.
- **Privacy-by-Design Architecture** — Stores user profiles and chat history strictly in local browser storage (`localStorage` / `IndexedDB`) with zero server-side personal data retention and optional per-session AI toggles.

### Tech Stack

| Layer         | Technology                   |
| ------------- | ---------------------------- |
| Frontend      | Next.js (React), Tailwind CSS, TypeScript |
| Backend       | Next.js API Routes (Stateless Proxy) |
| Database      | Cloudflare D1 (Public Job Market Samples) / IndexedDB (Local Import) |
| AI / Compute  | DeepSeek API (GenAI Engine)  |
| Hosting / Dev | Replit Cloud Platform        |

---

## Project Structure

```
.
├── docs/                    # Screenshots, architecture diagrams
├── src/
│   ├── app/                 # Next.js frontend pages & components
│   └── api/                 # API routes for proxying DeepSeek
├── submission/              # Required submission documents
│   ├── REPLIT PROOF OF USE.pdf
│   └── Submission Template SDC Hackathon.pdf
├── public/                  # Static assets & public datasets
├── .env.example             # Example environment variables
├── .gitignore
├── .replit                  # Replit run configuration
├── LICENSE
├── package.json             # Node dependencies
└── README.md
```

### Architecture

```
User Browser (Local Storage) ──► Replit (Next.js App / API Proxy) ──► DeepSeek API (Optional / User-Toggled)
                │
                └──► Cloudflare D1 (Public Job Market Samples)
```

---

## How to Run

### Run on Replit (Recommended)

1. Open the [Replit Project](https://nextep-ericyywies.replit.app), or import this repository via **Create Repl → Import from GitHub**.
2. Open the **Secrets** tab (🔒) and add your environment variables:
   - `DEEPSEEK_API_KEY`
3. Click **Run**. Replit will install dependencies and start the Next.js development/production server.

---

## How We Use Replit *(Required)*

- **Development:** Collaborative coding and live multi-developer prototyping using Replit's shared workspace.
- **Hosting:** The full-stack Next.js application is deployed directly on Replit Cloud Platform (`https://nextep-ericyywies.replit.app`).
- **Secrets Management:** Securely storing API keys (e.g., DeepSeek API keys) using Replit Secrets.

📄 Proof of use: [`Submission/REPLIT PROOF OF USE.pdf`](Submission/REPLIT%20PROOF%20OF%20USE.pdf)

---

## Challenges & Learnings

- **Challenge:** Balancing intelligent AI personalization with strict user data privacy requirements.
- **Solution:** Designed a client-side state architecture (`localStorage`) where personal profiles and CV parsing remain in the browser, and DeepSeek API calls require explicit, per-session user consent with zero server-side logging.

## Future Improvements

- [ ] Integrate more localized EEE internship and green energy job datasets.
- [ ] Enhance interactive milestone tracking with automated certificate verification.

## Team

| Name        | Role                | GitHub                                   |
| ----------- | ------------------- | ---------------------------------------- |
| Yue XIONGHE | Team Lead / Full-Stack | [@ERYCYUE](https://github.com/ERYCYUE) |
| GONG SHENGYUE | AI & Data Pipeline  | [@username](https://github.com/username) |
| YING ZICHEN | Frontend & UI       | [@username](https://github.com/username) |
| CHEN HAOYU | Testing & Doc       | [@username](https://github.com/username) |

---

## Submission Checklist

- [x] Team name, domain (Domain 1) and SDG track filled in
- [x] Slide deck link added
- [x] Demo video link added
- [x] Replit used, with proof of use in `submission/`
- [x] Submission template completed in `submission/`
- [x] "How to Run" steps verified
- [x] No API keys or secrets committed to the repository

## License

This project is licensed under the [Apache License 2.0](LICENSE).
