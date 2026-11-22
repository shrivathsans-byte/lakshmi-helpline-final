**Lakshmi: Government schemes over a phone call (Problem FAQ)**

**Summary**
India has 14.9Cr people aged 60+ (10.5% of the population in 2022), and 71% of them live in rural areas. Only 55% of older people know the old age pension exists, and only ~30% of eligible poor older people receive it. Many of these people have a basic phone, no apps and no habit of using AI, and they are wary of unknown voices because most fraud reaches them by phone. We want to give them one trusted number to call that tells them which schemes they can get, what to bring and where to go.

In this FAQ, we will a) determine the objective and target user, b) understand how people find out about schemes today, c) identify the challenges and their scale, d) propose the Lakshmi experience, and e) set up a pilot with success metrics.

**FAQs**

**Q1. What is our objective and who are we targeting?**
Our objective is to increase the # of eligible people who start a claim for a government scheme they are entitled to but not receiving. We are targeting people in Tier 2/3 towns and villages who a) are aged 60+, or are family members calling for them, b) have a basic phone or a smartphone they use only for calls and video, c) have never used an AI tool, or don't trust one, and d) are eligible for at least one of i) Ayushman Bharat health cover ii) old age pension iii) PM-Kisan income support. (Ex: a 72-year-old in a village outside Trichy whose son works in Chennai.)

**Q2. How do people find out about schemes today? What are the challenges in this?**
We observe that people find out about schemes through four routes, each with a gap:
a) **Word of mouth** (neighbours, relatives): We understand this is the most trusted route but is often wrong or incomplete. (Ex: "Pension is only for widows")
b) **Panchayat / local officials:** Trusted, but only available when visited, and coverage depends on the official.
c) **Common Service Centre (CSC) operators / agents:** Helpful, but some charge fees for free services, and the caller must already know which scheme to ask for.
d) **Government websites and apps:** These assume literacy, a smartphone and data, which this segment often lacks.
We infer that **the gap is not only "I don't know the scheme exists" but also "I don't know if I qualify, what to bring, or where to go"**. (Ex: The Dvara study found beneficiaries get stuck at several stages after enrolling, not only at awareness.)

**Q3. How big is this problem?**
a) **Old age pension:** We observe 2.21Cr older people receive it (Nov 2025), yet only ~30% of eligible poor older people receive it and only 55% know it exists. The central share is ₹200/month (ages 60–79) and ₹500/month (80+), plus a state top-up.
b) **Ayushman Bharat for 70+:** Since Oct 2024, every person aged 70+ gets ₹5 lakh/year of free hospital treatment, irrespective of income. We observe ~96L cards were issued by Dec 2025, against an eligible base of ~6Cr people aged 70+ (~16% enrolled). We understand most families don't know age is the only criterion.
c) **Informal workers:** We observe ~31Cr registered on e-Shram against an estimated ~40Cr informal workers.
We infer that **the eligibility-to-benefit gap runs into crores of people and is largest among older, rural, low-literacy people**.

**Q4. Why a phone call and not an app?**
a) We observe India has 958Mn internet users, 57% of them rural, but the people left out are older adults, rural women (nearly half don't own a phone) and ~350Mn feature-phone users (2023).
b) We observe voice helplines already work for this segment. (Ex: Kisan Call Centre has taken farmer calls in regional languages since 2004, with 84% satisfaction.)
c) **Our mental model is: meet the user on the device and habit they already have, which is dialling a number and talking.**

**Q5. Why are these users wary of AI, and how do we earn trust?**
We observe there is no published survey of AI fear among Tier 2/3 and rural adults. We infer the wariness comes from a) unfamiliarity: they have never been told what AI is, and b) fraud: the 1930 cyber-fraud helpline received 3.24Cr calls in 2025, and most scams start with an unknown voice on the phone.
We suggest Lakshmi earns trust by:
a) **Never asking for money, OTPs, bank details or Aadhaar numbers**, and saying so in the first ten seconds.
b) Leading with being helpful, not with AI. It is honest when asked. (Ex: "I am a computer helper, not a person")
c) Only informing, never applying on the caller's behalf, and always pointing to an official office and helpline. (Ex: 14555 for Ayushman Bharat)
d) Sending an SMS summary the caller can show a family member or official.

**Q6. When do people need this?**
We understand people look for scheme information at specific moments:
a) **Turning 60 or 70:** they become newly eligible but are not told.
b) **A hospital visit:** a family is facing a bill and doesn't know a 70+ member is covered.
c) **A missed payment:** a pension or PM-Kisan instalment hasn't arrived.
d) **A relative's prompt:** a son or daughter in a city hears about a scheme and calls on a parent's behalf.

**Q7. What is the suggested approach?**
We hypothesize that by giving people one number to call, where they answer 4–5 simple questions and hear which schemes they qualify for, what to bring and where to go, we will increase the # of eligible people who visit an official office to claim a scheme.
Call flow:
a) **Greeting and trust line:** who Lakshmi is and what it will never ask for.
b) **Questions:** age, state, ration card type, farmland ownership, anyone aged 70+ at home.
c) **Answer:** one scheme at a time: i) what you get ii) documents to bring iii) where to go iv) official helpline.
d) **Close:** repeat the key points and send an SMS summary.

**Q8. Which schemes will we cover and why?**
a) **Ayushman Bharat for 70+:** the simplest rule (age only) and the biggest awareness gap, so it gives the biggest "I didn't know" moment.
b) **Old age pension:** directly serves the core segment, with a proven gap between eligibility and receipt.
c) **PM-Kisan:** covers farm families, the largest working-age rural group.
We will not cover state-specific schemes in the first version, since rules differ by state.

**Q9. What will we not do?**
a) We will not collect money, OTPs, Aadhaar or bank details.
b) We will not apply for or enrol anyone in a scheme.
c) We will not give medical, legal or financial advice beyond scheme eligibility.
d) We will not guess. When unsure, Lakshmi says so and gives the official helpline.

**Requirements**

| S.No | Requirements | UXD |
|---|---|---|
| 1 | As a caller, when I dial the number, I should hear a greeting that says who Lakshmi is and that it will never ask for money, OTPs or bank details. **Language:** English and Tamil in the first version; Hindi and other Indian languages to follow. | |
| 2 | As a caller, I should be asked at most 5 simple questions, one at a time. **Edge cases:** caller doesn't know their ration card type; caller is calling for a parent. | |
| 3 | As a caller, I should hear which schemes I qualify for, one at a time, with i) what I get ii) documents iii) where to go iv) official helpline. **Count:** at most 3 schemes per call. | |
| 4 | As a caller, for each scheme I qualify for, I should be told where to go for more clarity. **Representation:** i) the office to visit (Ex: Common Service Centre, empanelled hospital, panchayat or block office) ii) the official helpline (Ex: 14555 for Ayushman Bharat, 155261 for PM-Kisan) iii) the documents to carry. **Edge cases:** if the caller shares their district, name the nearest office where we have that data; otherwise name the office type. | |
| 5 | As a caller, I should be able to interrupt, ask Lakshmi to repeat, or ask it to speak slower at any time. | |
| 6 | As a caller, at the end of the call I should receive an SMS summary. | |
| 7 | As a caller, when I ask something outside scheme eligibility, I should be told politely that Lakshmi can't help with it and given the right helpline. We should not i) guess eligibility ii) give medical or financial advice iii) ask for personal ID numbers. | |

**Analytics Requirements**

| S.No | Metrics to be tracked |
|---|---|
| 1 | # of calls, # of unique callers, call duration, language of call |
| 2 | Funnel: calls → questions completed → at least one eligible scheme found → SMS sent |
| 3 | # of eligible schemes found per caller, by scheme |
| 4 | Drop-off point in the call (greeting / questions / answer) |
| 5 | # of calls with an unanswered or out-of-scope question, by topic |
| 6 | Follow-up (pilot only): % of callers who visited an office within 30 days |

**Pilot Requirements**
**Hypothesis:** We hypothesise that by offering a trusted phone helpline for scheme eligibility, we will increase the # of eligible people who visit an official office to claim a scheme.
**Target audience:** People aged 60+ (or family members calling for them) in 2 Tier 2/3 districts: Tiruchirappalli (Trichy) and Madurai, Tamil Nadu.
**Recruitment:** Number shared through panchayats, ASHA workers and SMS.
**Platform:** Phone call (any phone).
**Duration:** 30 days.
**Primary goal:** % of callers who visit an official office to claim at least one scheme within 30 days.
**Secondary goals:**
1. % of calls that complete the questions
2. % of callers found eligible for at least one scheme they don't receive
3. % of callers who call again or share the number
4. Caller-reported trust ("Would you tell a neighbour about this number?")

**Appendix**
A. Sources
- UNFPA India Ageing Report 2023 (14.9Cr aged 60+, 71% rural): https://india.unfpa.org/sites/default/files/pub-pdf/iar_2023_rgb_web.pdf
- Old age pension awareness (55%): https://www.businesstoday.in/personal-finance/retirement-planning/story/29-senior-citizens-have-access-to-social-security-schemes-like-pension-pf-report-433430-2024-06-15
- Old age pension uptake among poor older people (~30%): https://www.downtoearth.org.in/news/economy/less-than-a-third-bpl-senior-citizens-benefit-from-old-age-pension-scheme-health-ministry-survey-74962
- Old age pension beneficiaries (2.21Cr): https://static.pib.gov.in/WriteReadData/specificdocs/documents/2025/nov/doc2025117686801.pdf
- Ayushman Bharat 70+ eligibility: https://pib.gov.in/PressReleasePage.aspx?PRID=2082288
- Ayushman Bharat 70+ eligible base (~6Cr people, 4.5Cr families): https://www.pmindia.gov.in/en/news_updates/cabinet-approves-health-coverage-to-all-senior-citizens-of-the-age-70-years-and-above-irrespective-of-income-under-ayushman-bharat-pradhan-mantri-jan-arogya-yojana-ab-pm-jay/
- Ayushman Bharat 70+ cards (~96L): https://www.deccanherald.com/dhie/news-and-trends/2026/02/03/over-96-lakh-seniors-enrolled-in-ayushman-vay-vandana-scheme
- e-Shram coverage: https://www.theindiaforum.in/sites/default/files/article_pdf/2026/08/10/2074-1786335210.pdf
- Dvara study on beneficiaries: https://theprint.in/india/despite-direct-benefit-transfers-welfare-schemes-beneficiaries-still-floundering-claims-study/983113
- Internet users (IAMAI 2025): https://yourstory.com/2026/01/indias-internet-user-base-crosses-950-million-2025-iamai-report
- Feature-phone users: https://techcrunch.com/?p=2806846
- Rural women's phone ownership: https://www.business-standard.com/india-news/digital-india-divide-nso-rural-women-mobile-phone-ownership-gap-125052901804_1.html
- 1930 helpline calls: https://the420.in/india-cybercrime-1930-helpline-complaints-2025-digital-fraud-alarm/
- Kisan Call Centre: https://tci.cornell.edu/?p=9237
