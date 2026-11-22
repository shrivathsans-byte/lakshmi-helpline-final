# Lakshmi: government schemes over a phone call

A free voice helpline that helps older people in Tier 2/3 India, and family members calling for them, find out **which government schemes they can get, what to carry and where to go**. It speaks **English and Tamil**, never asks for Aadhaar, OTPs, bank details or money, and is piloted for **Tiruchirappalli (Trichy) and Madurai, Tamil Nadu**.

Built at Builders' Day, Product (Un)Conference '26, Bengaluru, for the request "An AI Assistant over a Phone Call".

**Live demo and one-pager:** `<add your Netlify link here>`

## The problem
- 14.9 crore Indians are 60+, and 71% live in rural areas (UNFPA India Ageing Report 2023).
- Only ~16% of the ~6 crore people eligible for Ayushman Bharat 70+ (free hospital care up to ₹5 lakh a year) had enrolled by Dec 2025.
- Only ~30% of eligible poor older people get the old age pension, and only 55% know it exists.
- Most fraud reaches this group by phone (3.24 crore calls to the 1930 cyber-fraud helpline in 2025), so trust comes first.

The gap is not just awareness: people don't know **whether they qualify, what to bring, or where to go**. Full problem write-up: [`docs/problem-statement-faq.md`](docs/problem-statement-faq.md).

## What Lakshmi does
1. Greets the caller, says it is a computer helper, and promises never to ask for money, Aadhaar, an OTP or bank details.
2. Listens first: urgent problems (someone in hospital now, a payment that hasn't come, a lost card, a suspicious call) are solved first.
3. Asks simple questions one at a time: age, district, ration card type, widow or disability, farmland, income tax or government job.
4. Names every scheme the person is likely eligible for, then explains each: what you get, documents to carry, where to go, the official helpline.
5. Closes with a reference code and asks consent for a follow-up call.

**Schemes covered:** Ayushman Bharat 70+, old age pension, widow pension, disability pension, Kalaignar Magalir Urimai Thogai, PM-Kisan, PMSBY accident insurance. Named hospitals and offices for Trichy and Madurai.

## How it's built
| Layer | Choice |
|---|---|
| Voice agent | ElevenLabs Agents (speech-to-text, turn-taking, text-to-speech) |
| Model | Claude Haiku 5.5 via ElevenLabs |
| Voices | Roohi (Indian English), Janani (Tamil); automatic language switching |
| Knowledge | Curated knowledge base from official sources ([`agent/knowledge-base.md`](agent/knowledge-base.md)) |
| Behaviour | System prompt ([`agent/system-prompt.md`](agent/system-prompt.md)) |
| Front end | Static page with the embedded ElevenLabs widget ([`site/`](site/)) |
| Production path | Indian phone number via Plivo SIP trunking, once number KYC and an India-hosted voice deployment are in place; Bhashini for more Indian languages |

## Trust, safety and evals
- **48 of 48** automated test runs pass on the live agent: 24 scripted callers, each run twice ([`agent/evals.md`](agent/evals.md)).
- Test areas: right schemes, personal data and trust, fraud, safety, real problems, and difficult callers (off-topic, abuse, other languages).
- Guardrails block any reply that asks for or repeats an Aadhaar number, OTP, bank details or money, and block prompt-injection attacks.
- Safety routes: emergency → 108, distress → Tele-MANAS 14416, elder abuse → Elder Line 14567, fraud → 1930.
- Every real call is scored afterwards on five checks (no personal data asked, official next step given, eligibility correct, safety handled, no false authority).
- Limits: 10-minute calls, 5 at a time, 200 a day; transcripts deleted after 30 days.

## Repository
```
agent/   system prompt, knowledge base, eval results, agent configuration
docs/    problem statement (FAQ format)
site/    the public demo page and one-pager
```

## Limitations
- Eligibility is "likely", based on what the caller says; the office confirms.
- Scheme amounts are Tamil Nadu rates and can change. Magalir Urimai Thogai rules and some helpline numbers (Elder Line 14567, CM helpline 1100) should be re-confirmed from official sources.
- The demo runs in the browser; no real phone number or SMS yet.
