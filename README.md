<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0969DA,100:0d1117&height=180&section=header&text=Abderrazek%20Ben%20Cheikh%20Souguir&fontSize=34&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full-stack%20engineer%20%C2%B7%20Founder%20of%20FirstDig&descAlignY=60&descSize=16" />

[![FirstDig](https://img.shields.io/badge/Live-firstdig.net-0969DA?style=flat)](https://firstdig.net)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/abderrazek-ben-cheikh-souguir-803743233/)

</div>

I build complete products on my own: database, backend, workers, web and mobile apps, payments, deployment.
Most of my work is in private repositories, so this page shows what it does rather than the code.

## Now: FirstDig

**[firstdig.net](https://firstdig.net)** emails US service businesses (pool builders, roofers, solar, HVAC, fences…)
the new building permits in the areas they draw on a map, every morning, every week or within the hour.

- **Ingestion:** 100 city open-data feeds in 29 states and DC (Socrata, ArcGIS, CKAN, CSV), normalized into one schema,
  geocoded and sorted into 18 trades. 1.6M+ permits, about 110,000 new ones a month
- **Delivery:** PostGIS zone matching, idempotent digests, an email outbox with retries, bounce and complaint webhooks
- **Product:** job-finished alerts, ready-date estimates (Kaplan–Meier), busiest streets, a door-to-door route planner,
  AI summaries through the OpenAI Batch API with a monthly budget stop
- **AI assistants:** an MCP server and OAuth so customers can ask ChatGPT or Claude about their permits
- **Business:** Stripe Checkout, Customer Portal and webhooks, plans and limits editable by admins, a reverse trial
- **Ops:** a stateless API and a separate worker, zero-downtime deploys from GitHub Actions on my own server,
  crawler-ready public pages (2,500+ city, state and monthly report pages)

`FastAPI` `PostgreSQL + PostGIS` `React 19` `TypeScript` `Stripe` `MCP` `Docker` `GitHub Actions`

## Before that

| Project | What it does | Stack |
|---|---|---|
| **Tourism and hospitality platform** | Mobile app, merchant dashboard and backend: bookings, loyalty rewards, a multi-agent AI assistant | FastAPI · PostgreSQL · Flutter · React · RabbitMQ · AWS |
| **B2B commodity trading marketplace** | Deal rooms, live bidding, shipping workflows and contracts for buyers, sellers and admins | FastAPI · PostgreSQL · React · Docker · AWS |
| **Property management system** | Delivered to a paying client: bookings, tenants, finances, reporting; built to be white-labelled | FastAPI · PostgreSQL · React · Docker |
| **AI video processing pipeline** | Video in, report out: transcoding, speaker diarization, translation, agent analysis, PDF reports | Python · FFmpeg · CrewAI · RabbitMQ · AWS |
| **[Enigma's Echo](https://github.com/Rezayek/Enigma-s-echo-source-code)** | Puzzle-driven mystery adventure game (internship) | Unity · C# · Blender |

## Tools I use most

**Backend** Python, FastAPI, PostgreSQL / PostGIS, RabbitMQ, Stripe
**Frontend and mobile** TypeScript, React, Flutter / Dart
**AI** OpenAI API and Agents SDK, MCP, CrewAI
**Infrastructure** Docker, GitHub Actions, AWS, nginx

## Contact

Open to freelance work on full-stack products and AI integrations.
[LinkedIn](https://www.linkedin.com/in/abderrazek-ben-cheikh-souguir-803743233/) · [firstdig.net](https://firstdig.net)
