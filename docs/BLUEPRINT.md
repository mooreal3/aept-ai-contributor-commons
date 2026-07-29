# AEPT-AI Contributor Commons

## License, compensation, evidence, and enterprise monetization blueprint

- **Decision date:** July 29, 2026
- **Verdict:** GO WITH CHANGES for a non-token, U.S.-only pilot
- **Confidence:** High on the licensing boundary and pilot direction; medium on final entity, tax, securities, worker-classification, and professional-services treatment until the facts and contract language are fixed

> This is a product and governance blueprint, not legal, tax, accounting, or securities advice. Open-source counsel, corporate counsel, a CPA, and the applicable licensed professionals must approve the instruments and claims before launch.

## The shortest answer

Apache is not the license you remember.

No standard open-source license gives contributors a future share of enterprise revenue. Apache-2.0 grants broad, royalty-free copyright and patent permissions. It does not create contributor compensation, equity, royalties, or ownership in the project.

The viable model has separate layers:

1. A public code license.
2. A contributor IP agreement.
3. A contributor compensation plan and signed award contract.
4. A scoring, review, correction, and appeal policy.
5. Separate free-tier terms and enterprise contracts.
6. A private identity, tax, sanctions, and payout workflow.

The cryptographic ledger records evidence and makes later rewriting detectable. It does not prove authorship, identity, originality, legal ownership, contribution value, or entitlement by itself.

## The non-negotiable licensing fork

You must choose which promise controls.

| Controlling promise | Recommended code model | What it permits | Honest label |
|---|---|---|---|
| True open source matters most | AGPL-3.0 plus a commercial alternative | Anyone may use it without paying if they comply with AGPL; buyers can pay for proprietary terms, warranties, hosting, support, or indemnity | Open source |
| Enterprises must pay for production use | BSL 1.1 with a carefully drafted Additional Use Grant for qualifying free use and later AGPL conversion | Personal, community, or qualifying SMB use can be free; larger production use requires a commercial license | Source-available until conversion |
| Maximum adoption matters most | Apache-2.0 public core plus proprietary enterprise modules and services | Anyone, including enterprises, may use the public core commercially; revenue comes from adjacent value | Open source core, proprietary enterprise layer |

An OSI-approved license cannot discriminate against commercial or enterprise use or require royalties merely for use. AGPL can require source availability for modified network software, but it cannot force an enterprise to buy a license. BSL can create the commercial boundary, but it is not open source before its change date.

SSPL is also source-available, not OSI-approved open source, and is broader than this project appears to need.

### My recommendation

Use one of these two routes:

**Route A, open-source first:** AGPL-3.0 core plus a paid commercial alternative. Choose this if the same codebase is the product and buyers are likely to pay to avoid reciprocal source obligations.

**Route B, enterprise-payment first:** BSL 1.1 with a narrow Additional Use Grant and later AGPL conversion. Choose this if free individual and SMB access plus mandatory enterprise licensing is the product promise.

Do not choose Apache-2.0 if the business model depends on compelling payment for use of the same public core. Apache can still work when the enterprise value is hosting, proprietary modules, support, certification, compliance, warranties, indemnity, or service levels.

## The legal instrument stack

These are distinct relationships and should not be collapsed into one click-through agreement.

| Instrument | Governs | Required result |
|---|---|---|
| Outbound repository license | Public use, modification, and redistribution | Clear public rights and limitations |
| Individual and corporate contributor agreement | Copyright and patent provenance; project rights to sublicense and commercially relicense | Contributors retain copyright by default while the steward receives sufficient commercial rights |
| Contributor Participation and Compensation Agreement | Eligibility, score use, award process, pool rules, taxes, disputes, termination, and no automatic token or equity rights | Economic participation is contractual and separate from copyright title |
| Scoring and appeals charter | Rubrics, evidence, review independence, conflicts, correction, appeal, and policy versioning | Reproducible and contestable decisions |
| Free-tier terms, privacy notice, and AUP | Hosted individual, consumer, and SMB use | Clear quotas, data practices, and account rules |
| Enterprise commercial license, MSA, order form, SLA, and DPA | Paid use, support, compliance, data processing, warranties, and indemnity | Enterprise rights and service obligations |
| Individual award notice | The approved amount, currency, conditions, and payout timing | The first event that creates a payable obligation, subject to counsel's drafting |

A DCO is useful provenance evidence but is not a contract or license. It is not enough if AEPT-AI needs to issue commercial alternatives. A customized CLA modeled on established individual and corporate contributor agreements is the better base.

Fractional copyright ownership is not recommended. It creates chain-of-title, relicensing, enforcement, inheritance, acquisition, and contributor-exit problems. Contributors can retain copyright while receiving a separate contractual economic benefit.

## Recommended operating model

### Project steward

Start with one U.S. for-profit operating entity. Contributors remain licensors or separately classified service providers, not automatic members, partners, shareholders, or token holders.

A cooperative may become attractive later, but it introduces state cooperative law, patronage, member governance, tax reporting, and possible securities questions. A charity is a poor direct profit-sharing vehicle because of private-inurement limits. A DAO or project token is not appropriate for the pilot.

### Separation of duties

```text
Project Steward
├── Maintainer Council: accepts technical work
├── Contribution Review Committee: applies the scoring rubric
├── Independent Appeals Panel: hears attribution and scoring appeals
├── Compensation Committee: nominates and approves awards
├── Legal Gatekeeper: IP, contracts, jurisdiction, and worker classification
└── CPA and Finance Controller: tax status, accounting, and reconciliation
```

No person should accept the contribution, set its final score, decide its appeal, and release its payment. Meaningful awards require two-person approval.

## Contribution and award lifecycle

```text
Contributor onboarding
  -> versioned contributor agreement
  -> repository contribution
  -> technical validation and maintainer acceptance
  -> evidence snapshot
  -> deterministic provisional score
  -> outcome observation window
  -> two independent reviews
  -> final score and signed receipt
  -> appeal window
  -> cohort award nomination
  -> legal, tax, budget, and sanctions gates
  -> two-person approval
  -> signed award notice
  -> fiat payment and reconciliation
```

Scores, award weights, and payable amounts must be different data fields.

- A score recognizes contribution merit.
- An award weight helps allocate a declared pool.
- An approved amount becomes payable only after the required approvals and signed notice.

This separation reduces the risk that every score is treated as a debt, wage, royalty, equity interest, or investment-like instrument.

## Contribution scoring

Do not reward raw commit counts, lines of code, popularity, or self-reported hours. Measure code, tests, documentation, design, security, review, operations, accessibility, and community work against category-specific evidence.

A pilot formula:

```text
merit_score =
  round(20 * (
    0.30 * impact +
    0.25 * quality +
    0.20 * difficulty_or_scarcity +
    0.15 * verifiability +
    0.10 * stewardship
  ))
```

Each component uses an anchored 0-to-5 rubric.

Controls:

- Sign and version the rubric, weights, examples, observation window, and effective date.
- Require two independent reviewers.
- Trigger a third reviewer if total scores differ by more than 15 points or any axis differs by more than 2.
- Record the evidence hashes, rubric version, scoring-code digest, reviewer decisions, and final result.
- Apply policy changes prospectively by default.
- Permit 30 days for an appeal based on missing evidence, rubric error, conflict of interest, mistaken attribution, or duplicate ownership.
- Use an LLM only to summarize evidence or identify anomalies. It must not set an authoritative score, award, legal status, or tax status.

### Pilot economics

Begin with a fixed, board-approved quarterly cash pool. Points are nontransferable, nonmarketable, and have no promised conversion rate.

For a declared cohort:

```text
recommended_award_i =
  declared_pool *
  eligible_weight_i /
  sum(all_eligible_weights)
```

The committee may apply documented caps, minimums, fraud holds, conflicts, and legal or tax exclusions. Every deviation needs a reason code and an appeal path.

If AEPT-AI later wants a true contractual percentage of enterprise receipts, counsel should define the exact revenue base, exclusions, caps, duration, vesting, forfeiture, change control, audit rights, unclaimed-property handling, and termination. Avoid the vague word "profits." A transferable or passive profit-linked interest may raise securities concerns even without a blockchain.

## Evidence ledger

Use a normal transactional system plus a tamper-evident transparency layer:

```text
Git provider and DocuSeal
          |
 signed webhook gateway
          |
 contribution case and policy engine
          |
 transactional outbox
          |
 append-only event writer
        /   \
private log  signed Merkle checkpoint
        \   /
 WORM archive and independent witness
```

Recommended baseline:

- PostgreSQL domain data and transactional outbox.
- Canonical JSON event serialization.
- SHA-256 event commitments and previous-hash links.
- Periodic Merkle roots.
- KMS or HSM-backed checkpoint signatures.
- Checkpoints copied to immutable storage and at least one independent timestamp or transparency witness.
- Open verification utility and contributor inclusion receipts.
- Append corrections and reversals; never silently overwrite history.

A blockchain is not required. An unwitnessed hash chain can still be rewritten or forked by an administrator. Independent, signed checkpoints are what make equivocation detectable.

### Public receipt fields

- Opaque contributor and contribution identifiers
- Repository, commit, and accepted pull-request commitments
- Agreement and scoring-policy versions
- Evidence commitment
- Reviewer quorum and decision commitment
- Appeal or correction status
- Prior event hash
- Checkpoint and inclusion proof

### Never put on the immutable or public ledger

- SSNs, EINs, ITINs, W-9s, or W-8s
- Identity documents or sanctions results
- Bank or wallet details
- Signed contract PDFs
- Private security reports
- Legal or accounting work product
- Unredacted names or personal contact data without a separate lawful basis and explicit choice

Use a regulated identity, tax, and payout provider or an isolated restricted-data vault. The core system should store opaque references and status only.

If “fed .me” meant ID.me or another identity provider, verify the exact service before designing the adapter. A W-9 is tax certification, not identity proof. An SSN or EIN is a tax identifier, not a login credential.

## Tokens and stablecoins

Do not issue an AEPT contribution token in the pilot.

The current SEC digital-asset interpretation makes clear that token form does not erase the legal character of an underlying arrangement. A token awarded for services such as bug fixes is not within the release's no-consideration airdrop analysis. A transferable token linked to project growth, enterprise revenue, management efforts, or profit expectations creates serious securities risk.

A stablecoin can later be a payment rail for a U.S.-dollar-denominated, already approved obligation. It does not sanitize the obligation itself.

Any later stablecoin path needs:

- Securities and money-transmission analysis
- A regulated payout partner
- Identity and sanctions screening
- Wallet verification and travel-rule analysis where applicable
- Fiat-denominated award records and conversion quotes
- Tax valuation and reporting at payment time
- Country-by-country eligibility
- Contributor consent, fees, network, and transaction evidence

Calling work-linked foreign payments “donations” does not make them gifts or remove tax, labor, sanctions, or securities analysis.

## DocuSeal and contract execution

DocuSeal can be a strong agreement workflow and evidence adapter. Its audit certificate can record signer and event evidence. Electronic signatures generally cannot be denied legal effect solely because they are electronic.

That does not cure a defective contract, missing authority, poor identity assurance, consumer-consent failure, record-retention failure, worker misclassification, or an unlawful economic arrangement.

For every signed instrument:

- Counsel owns the template and version.
- Store a document hash, template version, signer authority, intent, consent, and authentication evidence.
- Preserve the final signed document and certificate in restricted storage.
- Re-fetch final status from the provider after validating the webhook.
- Require a corporate contributor agreement when an employer may own the work.
- Provide a retrieval and correction process.

## Law-firm and CPA services

The partnership concept can work if professional independence and claims are precise.

Recommended boundary:

- The law firm and CPA firm contract directly with the client for their professional work.
- The platform provides workflow, evidence, and optional referrals.
- State-specific counsel reviews fee sharing, referral compensation, conflicts, unauthorized-practice rules, marketing, privilege, and confidentiality.
- Each professional's engagement letter defines exactly what is reviewed and who makes the final decision.
- The platform never represents an automated output as legal advice or an audit opinion.

“Reviewed by a CPA” is not a harmless label. Preparation, compilation, review, examination, audit, and agreed-upon procedures are different engagements. Use the precise term that matches the signed engagement and work actually performed.

Large disclaimers do not repair a misleading headline claim. Prefer:

> The rules engine was tested against policy set X, version Y, effective on date Z. A licensed CPA performed the procedures described in the linked report. No audit, review, legal opinion, or guarantee is provided unless expressly stated in a separate signed engagement.

Do not claim blanket “IRC and U.S. GAAP compliance.” Compliance depends on entity facts, transactions, elections, controls, reporting period, jurisdiction, and professional scope.

## Capability-first platform design

Keep providers replaceable:

- `cap.identity.assure`
- `cap.agreement.execute`
- `cap.contribution.ingest`
- `cap.evidence.attest`
- `cap.score.compute`
- `cap.review.decide`
- `cap.appeal.resolve`
- `cap.ledger.append.verify`
- `cap.award.nominate.approve`
- `cap.payout.disburse`
- `cap.service.entitle`
- `cap.enterprise.contract`
- `cap.audit.export`

Each contract defines inputs, outputs, authorization, idempotency, emitted events, evidence requirements, and failure behavior. GitHub, DocuSeal, identity, ACH, tax, and any later stablecoin provider remain adapters rather than the source of business rules.

Recommended runtime for a pilot:

- TypeScript modular monolith
- Next.js contributor and reviewer portal
- PostgreSQL
- Background workers with a transactional outbox
- Deterministic scoring library with golden fixtures
- Object storage with retention controls
- KMS or HSM-backed signatures
- Provider adapters and manual continuity procedures

Microservices and blockchain add failure modes without solving the pilot's hardest problems, which are chain of title, fair scoring, identity privacy, professional accountability, and appeal governance.

## Minimal viable pilot

### Phase 0: legal and policy freeze

- Select AGPL dual-license or BSL route.
- Form the steward entity.
- Approve individual and corporate contributor agreements.
- Approve compensation, privacy, scoring, conflicts, corrections, and appeals policies.
- Approve free-tier terms and enterprise contract architecture.
- Complete worker-classification, tax, security, privacy, and vendor reviews.

No external merge or compensation marketing before this gate.

### Phase 1: 90-day shadow scoring

- One public repository.
- Invited contributors.
- Versioned DocuSeal agreements.
- Deterministic scoring, two-person review, and appeals.
- Append-only evidence and signed checkpoints.
- No cash promise, token, equity, royalty, or redemption.

Acceptance criteria:

- Replays produce identical scores.
- Duplicate events are suppressed.
- Inclusion proofs verify.
- No restricted data reaches the public log.
- Reviewer variance is measured and explained.

### Phase 2: capped U.S. cash awards

- Small verified U.S. cohort.
- Private identity and current tax onboarding.
- Fixed, preapproved U.S.-dollar budget.
- Signed individual award notices.
- Two-person approval and 100 percent finance reconciliation.

### Phase 3: enterprise beta

- Versioned free-tier entitlements.
- Enterprise commercial contracts, SLA, DPA, and billing.
- Release-level chain-of-title report mapping included contributions to current agreements.
- Board-approved contribution pool.

### Phase 4: international payout rails

- Counsel-approved country matrix.
- W-8, withholding, treaty, sanctions, worker, securities, and privacy controls.
- Fiat first.
- Stablecoin only as an optional rail for a fiat-denominated award through an approved provider.

### Phase 5: optional token study

This is a separate project requiring a written securities opinion, board approval, jurisdiction restrictions, custody and market-abuse controls, smart-contract audit, incident response, and tax treatment. Existing points must not automatically convert.

## Immediate decisions

1. Is true OSI open source more important than mandatory enterprise payment?
2. Will the enterprise product monetize the same code, or proprietary services and modules around the core?
3. Which U.S. entity will be the steward and contracting party?
4. Is the first pool a fixed award budget or a later, counsel-approved percentage of defined enterprise receipts?
5. Which contributions count, and who independently reviews and hears appeals?
6. What identity, tax, payout, and retention vendors may hold restricted data?
7. Which exact professional engagement can be marketed, and who signs the final work?

## Connected AEPT-AI alignment

The connected material supports, but does not itself legally validate, this design:

- The private GitHub productization draft already contemplated BSL, SSPL, and an open-core free tier. This blueprint corrects the label boundary: BSL and SSPL are source-available, and SSPL is not the recommended route.
- The connected Drive governance material already has entitlement records, metering concepts, and append-only audit patterns. Those patterns can be adapted from vendor entitlement tracking to contributor evidence, but the legal rights must come from signed instruments.
- The connected SharePoint IP-governance material reinforces the need for chain-of-title, patent, and disclosure gates before commercial releases. It is an internal research input, not legal authority.
- An agent layer may summarize evidence, flag anomalies, and prepare reviewer packets. It must not independently create IP rights, approve compensation, determine legal compliance, or release funds.

## Primary sources

### Open source and contributor rights

- [OSI Open Source Definition](https://opensource.org/osd)
- [OSI licensing FAQ](https://opensource.org/faq)
- [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html)
- [GNU AGPL-3.0](https://opensource.org/license/agpl-3.0)
- [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/)
- [Business Source License 1.1](https://mariadb.com/bsl11/)
- [PolyForm Small Business License](https://polyformproject.org/licenses/small-business/1.0.0)
- [OSI assessment of SSPL](https://opensource.org/blog/the-sspl-is-not-an-open-source-license)
- [Apache individual contributor agreement](https://www.apache.org/licenses/icla.pdf)
- [Developer Certificate of Origin](https://developercertificate.org/)
- [Linux Foundation contribution-mechanism guidance](https://bestpractices.linuxfoundation.org/ip/contribution-mechanisms-dco.html)
- [17 U.S.C. Sections 201 and 204](https://www.copyright.gov/title17/92chap2.html)

### Crypto, payments, tax, and sanctions

- [SEC 2026 interpretation on crypto assets](https://www.sec.gov/files/rules/interp/2026/33-11412.pdf)
- [Securities Act definition in 15 U.S.C. Section 77b](https://uscode.house.gov/view.xhtml?edition=prelim&num=0&req=granuleid%3AUSC-prelim-title15-section77b)
- [FinCEN convertible virtual currency guidance](https://www.fincen.gov/resources/statutes-regulations/guidance/application-fincens-regulations-persons-administering)
- [IRS digital-asset transaction FAQ](https://www.irs.gov/individuals/international-taxpayers/frequently-asked-questions-on-digital-asset-transactions)
- [IRS Form W-9](https://www.irs.gov/pub/irs-pdf/fw9.pdf)
- [IRS foreign beneficial-owner forms](https://www.irs.gov/individuals/international-taxpayers/forms-for-foreign-beneficial-owners)
- [OFAC virtual-currency compliance guidance](https://ofac.treasury.gov/system/files/126/virtual_currency_guidance_brochure.pdf)

### E-signature and professional services

- [Federal E-SIGN Act, 15 U.S.C. Section 7001](https://uscode.house.gov/view.xhtml?req=%28title%3A15+section%3A7001%28c%29+edition%3Aprelim%29)
- [DocuSeal signature certificate and audit log](https://www.docuseal.com/faq/what-is-the-certificate-of-signature-audit-log)
- [DocuSeal security](https://www.docuseal.com/security)
- [FTC advertising FAQ](https://www.ftc.gov/business-guidance/resources/advertising-faqs-guide-small-business)
- [IRS Circular 230](https://www.irs.gov/tax-professionals/office-of-professional-responsibility-and-circular-230)
- [AICPA preparation, compilation, and review engagement guide](https://www.aicpa-cima.com/cpe-learning/publication/preparation-compilation-and-review-engagements-guide-OPL)
- [ABA Model Rule 5.4](https://www.americanbar.org/groups/professional_responsibility/policy/ethics_2000_commission/e2k_rule54/)
- [ABA Model Rule 5.5](https://www.americanbar.org/groups/professional_responsibility/publications/model_rules_of_professional_conduct/rule_5_5_unauthorized_practice_of_law_multijurisdictional_practice_of_law/)
- [ABA Model Rule 7.2](https://www.americanbar.org/groups/professional_responsibility/publications/model_rules_of_professional_conduct/rule_7_2_advertising/)

ABA rules are models. The rules adopted in each relevant jurisdiction control.
