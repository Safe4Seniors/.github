# Safe4Seniors

**Voice AI wellness check-ins for seniors aging in place — no app, no internet, just a phone call.**

Safe4Seniors delivers daily AI-powered companion calls to older adults, monitoring health patterns and alerting caregivers to early warning signs. Built for rural and underserved communities where broadband access and tech literacy can't be assumed.

---

## What We Build

| Repo | Description |
|------|-------------|
| `core` | Voice AI call engine — Amazon Connect, NVIDIA Riva STT/TTS, Claude (Bedrock) |
| `platform` | HIPAA-compliant API, Amazon Connect + NVIDIA Riva on EC2 |
| `dashboard` | Caregiver and family portal — real-time alerts, trend visualization |
| `eval` | Test suite for the "Sunny" AI persona across senior interaction scenarios |
| `nimipuutímt` | Nez Perce language model — NVIDIA NeMo ASR/TTS fine-tuning |

---

## Architecture

```
Amazon Connect  →  NVIDIA Riva STT  →  Claude (Bedrock)  →  NVIDIA Riva TTS  →  Amazon Connect
                                              ↓
                                    Cloudflare D1 / R2
```

**Stack:** Python 3.12 · FastAPI · Cloudflare Workers/D1/R2/KV · AWS (EC2, Bedrock, Connect) · NVIDIA Riva

**Target latency:** < 3 seconds end-to-end per conversational turn

---

## Language Preservation

In partnership with the **Nez Perce Tribe**, we are building the first voice AI system capable of conducting wellness calls in Nimipuutímt (Nez Perce). This work is guided by a foundational principle of **data sovereignty** — the tribe owns all recordings and model weights. Storage is maintained in tribally-controlled Cloudflare R2.

This is not a feature. It is a parallel mission: elder wellness and language preservation are inseparable.

---

## Compliance

- HIPAA-compliant architecture — single BAA with AWS (Amazon Connect, Bedrock, EC2)
- TCPA-compliant outbound calling via Amazon Connect
- SOC 2 preparation in progress

---

## NVIDIA Inception

Safe4Seniors is a member of the **NVIDIA Inception Program** (joined February 2026), supporting our inference infrastructure for low-resource language model training and real-time voice AI.

---

## Organization

**Original Solutions LLC** · Lewis-Clark Valley, Idaho

- Jay Myers — Co-Founder & CEO
- Dr. Richard Stanley — Co-Founder (PhD, Oxford; global health IT, PATH, UNICEF)

---

## Contact

- Web: [safe4seniors.ai](https://safe4seniors.ai)
- Investment inquiries: [info@safe4seniors.ai](mailto:info@safe4seniors.ai)
- Tribal & academic partnerships: [info@safe4seniors.ai](mailto:info@safe4seniors.ai)

---

*Safe4Seniors is currently in pilot development. Seed round open — targeting Lewis-Clark Valley (rural/Medicare-Medicaid) and Wood River Valley (private-pay) as dual launch markets.*
