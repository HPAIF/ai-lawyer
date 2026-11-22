# Watchlist — laws & topics to research and monitor

> Baseline for an Armenian IT / SaaS company, copied into `ai-team/lawyer/watchlist.md` by
> `setup`. From then on the AI lawyer keeps the workspace copy current for this company: adds
> rows for the company's own sector and product modules, and updates statuses.
> Priority: P1 = before incorporation/first customer · P2 = within first months · P3 = when relevant.
> Status: lead (unverified) → researched (law card exists) → monitored.
> Leads were collected from secondary sources in 2026-11 and are **UNVERIFIED** until checked
> with `verify-law`. Trigger = the product module or company fact that makes a topic relevant.

## A. Company formation & governance — P1
| Topic | Acts to find in ARLIS | Status | Leads |
|---|---|---|---|
| Legal form, founding, charter | Civil Code (Քաղաքացիական օրենսգիրք); Law on Limited Liability Companies; Law on State Registration of Legal Entities | lead | — |
| Accounting & reporting | Law on Accounting; reporting obligations | lead | — |

## B. Tax (legal side; the accountant member owns the numbers) — P1
| Topic | Acts | Status | Leads |
|---|---|---|---|
| General tax regime, turnover tax, micro-business | Tax Code (Հարկային օրենսգիրք) | lead | — |
| IT / high-tech incentives | Tax Code + high-tech support legislation; hightech.gov.am | lead | Sources **conflict** (2026): some say the IT certificate regime was replaced by a "high-tech support regime" with a reduced turnover tax for High-Tech Registry companies; others still describe certificate benefits; payroll deductions/refunds for IT specialists also reported. Verify everything. ([lead](https://residentarmenia.com/en/it-tax-regime/), [lead](https://armenian-lawyer.com/taxes-armenia/), [lead](https://profin.am/en/it-sector-taxes-in-armenia-2026-guide-for-companies-individual-entrepreneurs-and-freelancers/)) |
| VAT on SaaS (domestic & export of services) | Tax Code | lead | — |
| E-invoicing | Tax Code; SRC rules | lead | — |

## C. Cash registers / fiscal — P1 if the product issues receipts or sits at a point of sale
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Cash register (ՀԴՄ) use, e-HDM / electronic cash register | Law on Application of Cash Registers (verify exact title); Government decision N 1976-Ն (reported); law HO-309-N (reported, in force 2027-01-01) | lead | Electronic registers reported to become an alternative to hardware ones from 2027; missing receipts are a frequent SRC enforcement target ([lead](https://finport.am/full_news.php?id=56708&lang=3), [lead](https://agenticglobaltax.com/armenia-armenia-tax-authority-publishes-july-2026/)). Key product question: can/must the software act as or integrate with a certified register? |

## D. Personal data — P1
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Processing, consent, notification, cross-border transfer | Law on Protection of Personal Data (2015) | lead | Regulator = Personal Data Protection Agency (MoJ). Draft reform (consultation ~Aug 2026) would create an independent Commission and move closer to GDPR, but no controller/processor split ([lead](https://lylegal.com/news/law-personal-data-protection-republic-armenia-key-proposed-amendments-and-their-comparition), [lead](https://csometer.info/updates/armenia-moves-towards-independent-data-protection-oversight-stronger-role-civil-society)) |
| GDPR | EU Reg. 2016/679 | lead | Only if EU customers / EU data subjects |

## E. Cybersecurity & information systems — P2
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Cybersecurity duties, critical information infrastructure | Law on Cybersecurity (adopted 2025-12-04, in force 2026-01-04 — ARLIS act 228265); Law on Regulation of Information Systems (in force 2025-12-26, reported) | lead | Sub-legislative acts due within 12 months; check which sectors are "vital" and whether customers become CII operators whose suppliers get obligations ([ARLIS](https://arlis.am/en/acts/228265), [lead](https://practiceguides.chambers.com/practice-guides/cybersecurity-2026/armenia)) |

## F. Contracts & e-commerce — P1
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Contract formation, liability caps, penalties, termination | Civil Code | lead | — |
| Electronic contracts & signatures | Law on Electronic Document and Electronic Digital Signature (verify title) | lead | — |
| Consumer protection (only if B2C) | Law on Consumer Rights Protection (verify title) | lead | — |
| Advertising / marketing messages | Law on Advertising | lead | — |

## G. Intellectual property — P2
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Software copyright, employee/contractor works | Law on Copyright and Related Rights | lead | — |
| Trademark | Law on Trademarks; aipo.am | lead | — |
| Open-source licences | (contract law + licence texts) | lead | — |

## H. Employment — P2
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Hiring, remote work, contractors vs employees | Labor Code (Աշխատանքային օրենսգիրք) | lead | — |
| Foreign specialists | Law on Foreigners; tax incentives | lead | — |

## I. The customers' sector (indirect) — P2
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Rules your customers must follow that the product touches (licences, safety, reporting, metrology of connected devices) | Government decisions; sector regulators; EAEU technical regulations | lead | Add one row per rule at setup, based on `ai-team/company/products/` |

## J. Competition — P2 if pricing features or concentrated markets
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Price information exchange between competing customers; dominant customers; exclusivity | Law on Protection of Economic Competition | lead | A price-monitoring feature can facilitate collusion — design review needed |

## K. Payments / loyalty — P3 unless money flows through the product
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Payment systems, e-money, prepaid cards, loyalty points | Law on Payment and Settlement Systems; CBA regulations; AML law | lead | — |

## L. AI — P3
| Topic | Acts | Status | Leads |
|---|---|---|---|
| AI rules | none in RA as of mid-2026 (reported); EU AI Act if EU market | lead | ([lead](https://www.levellers.ai/what-is/ai-regulation-armenia)) |

## M. Public procurement — P3 (if selling to state-owned customers or bodies)
| Topic | Acts | Status | Leads |
|---|---|---|---|
| Procurement rules | Law on Procurement; gnumner.am | lead | — |
