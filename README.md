import { useState } from “react”;

const NAVY = “#002147”;
const NAVY2 = “#1A3A5C”;
const GOLD = “#B8860B”;
const GOLDLT = “#F5E6B0”;
const CRIM = “#8B1A1A”;
const CRIMLT = “#FFF0F0”;
const WHITE = “#FFFFFF”;
const OFF = “#F8F8F6”;
const COAL = “#1E1E1E”;
const SLATE = “#4A4A4A”;

const slides = [
// ── SLIDE 1: COVER ──────────────────────────────────────────────────
{
id: 1,
type: “cover”,
tag: “INSTITUTIONAL SNAPSHOT”,
issue: “Issue No. CRCS 08 / 2026”,
title: “The Rohingya Crisis in March 2026”,
subtitle: “A Month of Converging Emergencies”,
body: “Food assistance restructured. Judicial history made in The Hague. Diplomatic stalemate entrenched. And a population of 1.2 million people awaiting a future that international inaction continues to defer.”,
meta: “Monthly Arakan Review  |  March 2026  |  Center for Rohingya Crisis Studies”,
swipe: “Swipe to read the full institutional snapshot →”,
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 2: CONTEXT ─────────────────────────────────────────────────
{
id: 2,
type: “context”,
tag: “CONTEXT”,
chapter: “Why This Month Matters”,
headline: “Three Crises, One Community, Zero Durable Solutions”,
paragraphs: [
“March 2026 did not produce a single catastrophic event. It produced something more insidious: the quiet normalisation of conditions that, in any other context, would be treated as a global emergency requiring immediate mobilisation.”,
“The World Food Programme announced a fundamental restructuring of food assistance for 1.2 million Rohingya refugees in Bangladesh, effective 1 April 2026. In Rakhine State, Myanmar, the Arakan Army continued to entrench governance structures that the UN Office of the High Commissioner for Human Rights has documented as systematically abusive toward Rohingya civilians. And at the International Court of Justice in The Hague, three weeks of oral arguments in the landmark genocide case concluded, placing the weight of decades of suffering into the formal record of international law.”,
“Each of these developments is significant on its own. Together, they reveal the full architecture of a crisis that the international community has repeatedly acknowledged and repeatedly failed to resolve.”,
],
stat: { number: “9th”, label: “Year of acute displacement without a credible political horizon” },
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 3: FOOD CRISIS ──────────────────────────────────────────────
{
id: 3,
type: “data”,
tag: “HUMANITARIAN CRISIS”,
chapter: “The Food Assistance Restructuring”,
headline: “Two-Thirds of Refugees Face Reduced Food Support from April 2026”,
paragraphs: [
“Throughout March 2026, WFP conducted camp-wide awareness activities to prepare approximately 1.2 million registered Rohingya beneficiaries for the new Targeting and Prioritization Exercise (TPE), effective 1 April 2026. The system replaces the previous universal rate of USD 12 per person per month with a three-tier vulnerability-graduated model.”,
“Under the TPE, approximately one-third of the population will maintain the USD 12 rate. The middle tier — estimated at roughly 50 per cent of beneficiaries — will receive USD 10 per month. The lowest tier, approximately 17 per cent, will receive just USD 7 per month. WFP states all tiers meet the 2,100 kcal per day minimum emergency standard. Bangladesh’s Refugee Relief and Repatriation Commissioner characterised the change as a ration cut, warning of potential law and order consequences.”,
“This restructuring does not occur in a vacuum. In 2023, WFP was forced to reduce rations from USD 12 to USD 8 due to a funding collapse. By November of that year, 90 per cent of camp residents had inadequate food consumption and the Global Acute Malnutrition rate among children reached 15.1 per cent, exceeding the WHO Emergency threshold. The TPE introduces a structural risk of replicating that trajectory for middle-tier households.”,
],
tiers: [
{ label: “Tier 1 (33%)”, value: “USD 12 / month”, note: “Extremely vulnerable: child/woman-headed households, elderly, disabled”, col: CRIM },
{ label: “Tier 2 (≈50%)”, value: “USD 10 / month”, note: “Moderate vulnerability — derived estimate, not independently stated”, col: GOLD },
{ label: “Tier 3 (17%)”, value: “USD 7 / month”, note: “Assessed as lower need — highest reduction”, col: NAVY2 },
],
note: “WFP global budget contracted by approximately 40% in 2025, driven primarily by US foreign aid reductions.”,
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 4: CAMP CONDITIONS ──────────────────────────────────────────
{
id: 4,
type: “analysis”,
tag: “CAMP CONDITIONS”,
chapter: “Cox’s Bazar: Life in the World’s Largest Refugee Settlement”,
headline: “1,182,755 People. Zero Right to Work. One Source of Survival Being Cut.”,
paragraphs: [
“As of 31 January 2026, Bangladesh hosted 1,182,755 registered Rohingya refugees from 245,998 families — a figure that includes 143,327 new arrivals since mid-2023. More than half are children. Approximately 235,000 children aged 5 to 17 remain outside formal schooling, exposed to elevated risks of trafficking, child labour, and early marriage.”,
“Rohingya refugees are legally prohibited from working in Bangladesh. They are almost entirely dependent on humanitarian assistance to survive. The psychological and economic effect of the TPE announcement rippled through camp communities throughout March. Dozens staged protests holding signs reading ‘Food is a right, not a choice.’ Multiple refugees interviewed by international media reported considering return to Myanmar despite documented safety risks, or irregular maritime departure to Malaysia — an extremely dangerous journey that has claimed hundreds of lives annually.”,
“A trafficking case involving a 12-year-old Rohingya child, publicised on 30 March 2026, exposed the transnational dimensions of criminal networks operating through the camps. This single case, while unconfirmed as representative of a broader pattern, illustrates the protection vulnerabilities that deepen as humanitarian conditions deteriorate and legal pathways to safety remain closed.”,
],
stats: [
{ number: “1.18M”, label: “Registered refugees in Bangladesh” },
{ number: “235K+”, label: “Children estimated out of school” },
{ number: “USD 934.5M”, label: “JRP funding required — critically underfunded” },
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 5: RAKHINE STATE ────────────────────────────────────────────
{
id: 5,
type: “crisis”,
tag: “RAKHINE STATE, MYANMAR”,
chapter: “The Crisis at the Source”,
headline: “Arakan Army Controls 14 of 17 Townships. Rohingya Civilians Bear the Cost.”,
paragraphs: [
“For the Rohingya who remain inside Myanmar — estimated at 600,000 to 630,000 people — March 2026 represented another month of entrenched, multi-actor persecution. The Arakan Army, which now exercises de facto administrative and military control over approximately 14 of 17 Rakhine State townships, has consolidated governance structures that the United Nations Office of the High Commissioner for Human Rights has documented as systematically exclusionary and abusive toward Rohingya civilians.”,
“OHCHR’s 2025 Annual Update, published on 2 March 2026, confirmed a year-long pattern of arbitrary arrest and detention, enforced disappearances, forced recruitment and forced labour, systematic extortion and confiscation of land, severe restrictions on movement requiring written AA authorisation to travel between villages, persistent institutional denial of Rohingya identity through compulsory use of the term ‘Bengali,’ and sustained obstruction of humanitarian access to Maungdaw and Buthidaung townships.”,
“The AA formally denies systematic targeting of Rohingya civilians. Available independent evidence, including documentation by Human Rights Watch, Amnesty International, and Fortify Rights, does not support this denial. OHCHR assessed that the documented pattern ‘may reflect an intention of the AA to motivate further displacement and cross-border movements to Bangladesh.’ The Myanmar military junta, meanwhile, retains localised aerial bombardment capacity and continued forced conscription of Rohingya males into proxy militia units, with over 5,000 conscriptions documented in the first half of 2025 alone.”,
],
nutrition: [
{ area: “Buthidaung Township”, phase: “Phase 5: CATASTROPHE”, detail: “Famine threshold — projected to May 2026”, col: CRIM },
{ area: “Maungdaw Township”, phase: “Phase 4: EMERGENCY”, detail: “Critical — projected to May 2026”, col: GOLD },
],
noteText: “Independent verification of conditions is precluded by communications blackouts imposed by both the junta and the AA.”,
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 6: REPATRIATION STALEMATE ───────────────────────────────────
{
id: 6,
type: “stalemate”,
tag: “REPATRIATION AND DIPLOMACY”,
chapter: “The Stalemate in Numbers”,
headline: “829,036 Files Shared. 354,751 Verified. Zero Returned.”,
paragraphs: [
“On 30 March 2026, Bangladesh’s Foreign Minister Dr Khalilur Rahman delivered a landmark parliamentary statement on the status of the repatriation process. The figures he presented are simultaneously a record of diplomatic effort and a measure of its complete failure to deliver safety for the people it concerns.”,
“Bangladesh has shared biometric and identification data on 829,036 Rohingya with Myanmar authorities across six sequential phases. Myanmar has verified approximately 354,751 of those individuals, of whom 253,964 are recognised as ‘persons previously residing in Myanmar.’ Yet not a single person has returned. The Foreign Minister confirmed that conditions in Rakhine State are not yet conducive to safe return.”,
“The Foreign Minister also invoked historical precedents — successful repatriations under bilateral agreements in 1978 and 1992 — as models for the current BNP administration’s approach. Analysts including the Observer Research Foundation and The Diplomat have cautioned that these comparisons are structurally inapplicable: those agreements were negotiated with a unified, internationally recognised central government with effective border control. Today, the entire Bangladesh-Myanmar border is administered by the Arakan Army, a non-state armed organisation with no recognised treaty-making capacity under international law.”,
],
pipeline: [
{ step: “Files Shared with Myanmar”, value: “829,036”, done: true },
{ step: “Individuals Verified by Myanmar”, value: “354,751”, done: true },
{ step: “Recognised as Former Residents”, value: “253,964”, done: true },
{ step: “Persons Actually Returned”, value: “ZERO”, done: false },
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 7: ICJ PROCEEDINGS ──────────────────────────────────────────
{
id: 7,
type: “justice”,
tag: “INTERNATIONAL JUSTICE”,
chapter: “The Gambia v. Myanmar: History in The Hague”,
headline: “Merits Hearings Concluded. The Court Now Deliberates on Whether Genocide Was Committed.”,
paragraphs: [
“The International Court of Justice’s three-week merits phase in the landmark case Application of the Convention on the Prevention and Punishment of the Crime of Genocide (The Gambia v. Myanmar) concluded on 29 January 2026 at the Peace Palace in The Hague. This represented the culmination of a legal process that began in November 2019, when The Gambia, on behalf of 57 members of the Organisation of Islamic Cooperation, filed the application accusing Myanmar of breaching the Genocide Convention through its treatment of the Rohingya.”,
“The hearings included two rounds of oral pleadings by both parties, testimony from three witnesses and one expert called by The Gambia, and testimony from one witness called by Myanmar. Eleven states participated as interveners — Canada, Denmark, France, Germany, the Netherlands, the United Kingdom, Maldives, Slovenia, the Democratic Republic of the Congo, Belgium, and Ireland — reflecting the broad recognition among state parties that the case carries implications for the interpretation of the Genocide Convention as a whole.”,
“UN Special Rapporteur Tom Andrews described the moment when Rohingya survivors testified before the Court as the ‘most important moment’ of the proceedings. He noted with significance that at no point during the hearings did Myanmar’s representatives use the word ‘Rohingya.’ The Court is now in deliberation. A legally binding judgment is expected later in 2026. East Asia Forum analysts assess it would, if decided in The Gambia’s favour, provide formal legal recognition of genocide and grounds for reparations — though enforcement within Myanmar under the current junta remains a substantial structural challenge.”,
],
timeline: [
{ year: “Nov 2019”, event: “The Gambia files application before ICJ” },
{ year: “Jan 2020”, event: “ICJ issues provisional measures — legally binding on Myanmar” },
{ year: “Jul 2022”, event: “ICJ rejects Myanmar’s preliminary objections; case proceeds” },
{ year: “Jan 2026”, event: “Merits hearings: 12–29 January, Peace Palace, The Hague” },
{ year: “2026”, event: “Judgment expected — legally binding, enforcement uncertain” },
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 8: ICC WARRANT ──────────────────────────────────────────────
{
id: 8,
type: “accountability”,
tag: “ACCOUNTABILITY”,
chapter: “ICC Arrest Warrant: Pending, Not Forgotten”,
headline: “An Application Has Been Filed Against the Man Who Is Now Myanmar’s President.”,
paragraphs: [
“On 27 November 2024, ICC Prosecutor Karim A.A. Khan KC filed an application for an arrest warrant for Senior General Min Aung Hlaing, Myanmar’s military commander-in-chief, covering the crimes against humanity of deportation and persecution of the Rohingya committed between 25 August and 31 December 2017. As of 31 March 2026, the Pre-Trial Chamber I had not issued any public decision on the application.”,
“Then, on 3 April 2026 — one day after the monitoring period — Min Aung Hlaing was voted Myanmar’s president by the junta-controlled parliament in elections dismissed by international observers as fraudulent. Amnesty International responded immediately, stating that ‘no individual should have immunity from prosecution for crimes under international law, no matter their position.’ The Burmese Rohingya Organisation UK warned that the development, combined with ongoing Arakan Army abuses, places any meaningful solution to the Rohingya crisis further out of reach.”,
“Separately, an Argentine federal court issued arrest warrants in February 2025 for 25 individuals including Min Aung Hlaing for crimes against humanity and genocide under the principle of universal jurisdiction — the first such proceeding against Myanmar in any national court. This parallel track, initiated by BROUK and six Rohingya survivors in 2019, signals that the architecture of international accountability, while slow, is expanding its reach.”,
],
tracks: [
{ body: “ICC”, status: “Application filed November 2024. Pre-Trial Chamber yet to rule publicly.”, color: NAVY },
{ body: “ICJ”, status: “Merits phase concluded. Judgment pending. Legally binding on Myanmar.”, color: GOLD },
{ body: “Argentina”, status: “Arrest warrants issued February 2025. First universal jurisdiction case.”, color: CRIM },
{ body: “IIMM”, status: “Ongoing evidence collection. Evidence shared with ICJ. Future prosecutions.”, color: NAVY2 },
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 9: REGIONAL ─────────────────────────────────────────────────
{
id: 9,
type: “regional”,
tag: “REGIONAL DYNAMICS”,
chapter: “Beyond the Camps: A Region in Denial”,
headline: “At Sea, in Detention, in Limbo. The Rohingya Diaspora Faces Closed Doors Across Asia.”,
paragraphs: [
“The Rohingya crisis does not end at the borders of Bangladesh. It extends across the Bay of Bengal, into the detention centres of India, and into the unresolved political calculations of ASEAN’s ten member states. March and April 2026 represent the peak of the Bay of Bengal’s calm-sea season. CRCS projects monthly maritime departure figures of 600 to 900 persons during this interval. OHCHR documented over 600 deaths and disappearances at sea in 2025 alone. No mandatory regional rescue or temporary protection framework exists.”,
“India, not a signatory to the 1951 Refugee Convention, continued its policy of detaining Rohingya individuals under the Foreigners Act. In May 2025, Indian authorities detained and deported at least 40 UNHCR-registered Rohingya refugees from Delhi, reportedly abandoning them in international waters near Myanmar. Multiple fatalities from drowning were reported. Human rights organisations characterised this as a violation of the customary international law principle of non-refoulement. Detention centre populations in Delhi and Hyderabad remained elevated throughout the March monitoring period.”,
“ASEAN’s Five-Point Consensus on Myanmar contains no specific provision for Rohingya civilian protection. The ASEAN Coordinating Centre for Humanitarian Assistance remains politically unable to operate in Rakhine State. March 2026 produced no new binding ASEAN mechanism. The United States, United Kingdom, and European Union issued no new targeted sanctions, diplomatic demarches, or emergency aid pledges specific to the Rohingya crisis during the monitoring period.”,
],
regions: [
{ name: “Bangladesh”, status: “1.18M refugees. Hosting burden unsustainable. No durable solution in sight.”, tone: “warn” },
{ name: “Myanmar / Rakhine”, status: “600K–630K Rohingya remaining. Arakan Army control. Near-total aid blockade.”, tone: “critical” },
{ name: “India”, status: “Continued detention and refoulement. Non-signatory to 1951 Convention.”, tone: “critical” },
{ name: “Malaysia / Indonesia”, status: “Maritime interceptions. Security framing over refugee protection. Non-refoulement breached.”, tone: “warn” },
{ name: “ASEAN”, status: “Five-Point Consensus excludes Rohingya. No operational capacity in Rakhine.”, tone: “neutral” },
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 10: RECOMMENDATIONS ─────────────────────────────────────────
{
id: 10,
type: “recommendations”,
tag: “STRATEGIC RECOMMENDATIONS”,
chapter: “What Must Happen Now”,
headline: “The Evidence Is Clear. The Obligations Are Established. What Is Missing Is Political Will.”,
paragraphs: [
“CRCS’s March 2026 monitoring yields four sets of evidence-based recommendations, directed at the actors with the power and the obligation to act. These are not aspirational requests. They reflect minimum obligations under international humanitarian law, international human rights law, and the principles of voluntary and dignified return that all relevant governments have formally endorsed.”,
],
recs: [
{
to: “Donor Governments and the UN”,
items: [
“Convene an emergency pledging conference for WFP Bangladesh operations and the 2025/26 Joint Response Plan within 30 days.”,
“Publicly reaffirm the obligation to enforce any ICC arrest warrant for Min Aung Hlaing, irrespective of his presidential status.”,
“Press for an independent humanitarian access corridor to northern Rakhine under verifiable protection guarantees.”,
]
},
{
to: “ASEAN and Regional Governments”,
items: [
“Adopt a binding maritime rescue and temporary protection protocol for Rohingya boat arrivals before the April to May 2026 peak season.”,
“Condition any repatriation framework engagement on verified, durable, and legally binding guarantees of Rohingya citizenship and security.”,
]
},
{
to: “Government of Bangladesh”,
items: [
“Establish a transparent TPE appeals mechanism before 1 April 2026 implementation to protect misclassified households.”,
“Ensure all repatriation communications explicitly present citizenship restoration, physical security, and land rights as non-negotiable prerequisites.”,
]
},
{
to: “Arakan Army”,
items: [
“Immediately lift movement restrictions, release arbitrarily detained individuals, cease forced recruitment, and restore humanitarian access to Maungdaw and Buthidaung.”,
“Make a public, concrete commitment to Rohingya citizenship and political participation — a minimum requirement of any credible governance claim over Rakhine State.”,
]
},
],
report: “Full Report: bit.ly/4bRqWxa”,
},

// ── SLIDE 11: CLOSING CTA ──────────────────────────────────────────────
{
id: 11,
type: “cta”,
tag: “READ THE FULL REPORT”,
headline: “The Rohingya Crisis Demands Sustained Attention, Rigorous Documentation, and Urgent Action.”,
body: “This institutional snapshot is drawn from CRCS Monthly Arakan Review Issue No. CRCS 08/2026 — a comprehensive, evidence-based, and academically rigorous monitoring report covering the period 1 to 31 March 2026. The full report includes 10 thematic chapters, 5 data tables, 18 footnotes, a verified media mapping output of 180-plus items, and strategic recommendations directed at all responsible actors.”,
callouts: [
“Access the full report to cite verified figures in your advocacy.”,
“Share this snapshot to amplify Rohingya voices in your network.”,
“Support CRCS to sustain independent documentation of this crisis.”,
],
link: “bit.ly/4bRqWxa”,
credit: “Center for Rohingya Crisis Studies (CRCS)  |  rocrcs@gmail.com”,
social: “Facebook  |  X  |  LinkedIn  |  Instagram  |  Bluesky”,
note: “All findings in this report are based on verified primary and secondary sources. No fabricated or assumed information is included.”,
},
];

// ── SLIDE RENDERERS ───────────────────────────────────────────────────────────

function CoverSlide({ s }) {
return (
<div style={{ background: NAVY, height: “100%”, display: “flex”, flexDirection: “column”, position: “relative”, overflow: “hidden” }}>
{/* Decorative gold stripe */}
<div style={{ height: 6, background: `linear-gradient(90deg, ${GOLD}, #E8C44A, ${GOLD})` }} />
<div style={{ flex: 1, display: “flex”, flexDirection: “column”, padding: “28px 28px 20px” }}>
{/* Tag */}
<div style={{ display: “flex”, alignItems: “center”, gap: 10, marginBottom: 20 }}>
<div style={{ width: 36, height: 36, background: CRIM, borderRadius: 4, display: “flex”, alignItems: “center”, justifyContent: “center” }}>
<span style={{ color: WHITE, fontSize: 14, fontWeight: 900 }}>C</span>
</div>
<div>
<div style={{ color: GOLD, fontSize: 9, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase” }}>{s.tag}</div>
<div style={{ color: “#8899BB”, fontSize: 9, letterSpacing: 1 }}>{s.issue}</div>
</div>
</div>
{/* Main title */}
<div style={{ borderLeft: `4px solid ${GOLD}`, paddingLeft: 16, marginBottom: 20 }}>
<div style={{ color: WHITE, fontSize: 22, fontWeight: 900, lineHeight: 1.2, marginBottom: 8 }}>{s.title}</div>
<div style={{ color: GOLD, fontSize: 13, fontStyle: “italic”, fontWeight: 500 }}>{s.subtitle}</div>
</div>
{/* Body */}
<div style={{ background: “rgba(255,255,255,0.06)”, borderRadius: 8, padding: “14px 16px”, marginBottom: “auto” }}>
<p style={{ color: “#C8D8EE”, fontSize: 12, lineHeight: 1.7, margin: 0 }}>{s.body}</p>
</div>
{/* Bottom */}
<div style={{ marginTop: 20, paddingTop: 16, borderTop: `1px solid rgba(255,255,255,0.12)` }}>
<div style={{ color: “#8899BB”, fontSize: 9, letterSpacing: 0.5, marginBottom: 8 }}>{s.meta}</div>
<div style={{ background: GOLD, borderRadius: 4, padding: “8px 14px”, display: “inline-block”, marginBottom: 10 }}>
<span style={{ color: NAVY, fontSize: 10, fontWeight: 800, letterSpacing: 0.5 }}>📖  {s.report}</span>
</div>
<div style={{ color: GOLD, fontSize: 10, fontWeight: 600 }}>{s.swipe}</div>
</div>
</div>
<div style={{ height: 4, background: CRIM }} />
</div>
);
}

function ContextSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: NAVY, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 17, fontWeight: 900, lineHeight: 1.2 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “16px 22px” }}>
<div style={{ color: NAVY, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 6 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11.5, lineHeight: 1.75, marginBottom: 14, textAlign: “justify” }}>{p}</p>
))}
{/* Stat callout */}
<div style={{ background: NAVY, borderRadius: 8, padding: “16px 20px”, display: “flex”, alignItems: “center”, gap: 16, marginTop: 4 }}>
<div style={{ color: GOLD, fontSize: 36, fontWeight: 900, lineHeight: 1 }}>{s.stat.number}</div>
<div style={{ color: “#C8D8EE”, fontSize: 11, lineHeight: 1.5 }}>{s.stat.label}</div>
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: NAVY, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function DataSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: CRIM, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLDLT, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 15, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: CRIM, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${CRIM}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
{/* Tier table */}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, letterSpacing: 1, textTransform: “uppercase”, marginBottom: 8 }}>WFP TPE Tier Structure (from 1 April 2026)</div>
{s.tiers.map((tier, i) => (
<div key={i} style={{ display: “flex”, alignItems: “stretch”, marginBottom: 6, borderRadius: 6, overflow: “hidden”, border: `1px solid ${tier.col}20` }}>
<div style={{ background: tier.col, width: 6, flexShrink: 0 }} />
<div style={{ flex: 1, background: WHITE, padding: “8px 12px” }}>
<div style={{ display: “flex”, justifyContent: “space-between”, alignItems: “baseline”, marginBottom: 2 }}>
<span style={{ color: tier.col, fontSize: 10, fontWeight: 800 }}>{tier.label}</span>
<span style={{ color: COAL, fontSize: 11, fontWeight: 700 }}>{tier.value}</span>
</div>
<div style={{ color: SLATE, fontSize: 9.5, lineHeight: 1.4 }}>{tier.note}</div>
</div>
</div>
))}
</div>
<div style={{ background: CRIMLT, border: `1px solid ${CRIM}40`, borderRadius: 6, padding: “8px 12px”, marginTop: 8 }}>
<span style={{ color: CRIM, fontSize: 9.5, fontStyle: “italic” }}>{s.note}</span>
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: CRIM, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function AnalysisSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: NAVY2, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 15, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: NAVY2, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ display: “grid”, gridTemplateColumns: “1fr 1fr 1fr”, gap: 8, marginTop: 6 }}>
{s.stats.map((st, i) => (
<div key={i} style={{ background: NAVY, borderRadius: 8, padding: “12px 8px”, textAlign: “center” }}>
<div style={{ color: GOLD, fontSize: 17, fontWeight: 900, lineHeight: 1.1, marginBottom: 4 }}>{st.number}</div>
<div style={{ color: “#C8D8EE”, fontSize: 9, lineHeight: 1.4 }}>{st.label}</div>
</div>
))}
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: NAVY, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function CrisisSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: “#2C0A0A”, padding: “16px 22px 12px”, borderBottom: `4px solid ${CRIM}` }}>
<div style={{ color: GOLDLT, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 15, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: CRIM, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${CRIM}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 8 }}>UN IPC Nutrition Phase Projections (Nov 2025 to May 2026)</div>
{s.nutrition.map((n, i) => (
<div key={i} style={{ display: “flex”, alignItems: “stretch”, marginBottom: 6, borderRadius: 6, overflow: “hidden”, border: `1px solid ${n.col}30` }}>
<div style={{ background: n.col, width: 6 }} />
<div style={{ flex: 1, background: WHITE, padding: “8px 12px” }}>
<div style={{ color: COAL, fontSize: 10, fontWeight: 700, marginBottom: 2 }}>{n.area}</div>
<div style={{ color: n.col, fontSize: 10, fontWeight: 800, marginBottom: 2 }}>{n.phase}</div>
<div style={{ color: SLATE, fontSize: 9 }}>{n.detail}</div>
</div>
</div>
))}
</div>
<div style={{ background: CRIMLT, border: `1px solid ${CRIM}40`, borderRadius: 6, padding: “8px 12px”, marginTop: 8 }}>
<span style={{ color: CRIM, fontSize: 9.5, fontStyle: “italic” }}>{s.noteText}</span>
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: CRIM, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function StaleSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: NAVY, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 15, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: NAVY, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 8 }}>The Repatriation Pipeline (Bangladesh FM Statement, 30 March 2026)</div>
{s.pipeline.map((item, i) => (
<div key={i} style={{ display: “flex”, alignItems: “center”, gap: 12, marginBottom: 8 }}>
<div style={{ width: 28, height: 28, borderRadius: “50%”, background: item.done ? NAVY : CRIM, display: “flex”, alignItems: “center”, justifyContent: “center”, flexShrink: 0 }}>
<span style={{ color: WHITE, fontSize: 10, fontWeight: 900 }}>{item.done ? “✓” : “✗”}</span>
</div>
<div style={{ flex: 1, background: item.done ? NAVYTL : CRIMLT, borderRadius: 6, padding: “8px 12px”, border: `1px solid ${item.done ? NAVY + "30" : CRIM + "30"}` }}>
<div style={{ color: SLATE, fontSize: 9, marginBottom: 2 }}>{item.step}</div>
<div style={{ color: item.done ? NAVY : CRIM, fontSize: 13, fontWeight: 900 }}>{item.value}</div>
</div>
</div>
))}
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: NAVY, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function JusticeSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: “#0A2040”, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 14, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: “#0A2040”, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 8 }}>Case Timeline: The Gambia v. Myanmar</div>
<div style={{ borderLeft: `3px solid ${GOLD}`, paddingLeft: 14 }}>
{s.timeline.map((item, i) => (
<div key={i} style={{ marginBottom: 10, position: “relative” }}>
<div style={{ position: “absolute”, left: -20, top: 2, width: 8, height: 8, borderRadius: “50%”, background: i === s.timeline.length - 1 ? GOLD : NAVY }} />
<div style={{ color: GOLD, fontSize: 9, fontWeight: 800, marginBottom: 1 }}>{item.year}</div>
<div style={{ color: COAL, fontSize: 10, lineHeight: 1.5 }}>{item.event}</div>
</div>
))}
</div>
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: NAVY, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function AccountSlide({ s }) {
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: CRIM, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLDLT, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 14, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: CRIM, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${CRIM}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 8 }}>International Accountability Mechanisms: Current Status</div>
{s.tracks.map((t, i) => (
<div key={i} style={{ display: “flex”, alignItems: “stretch”, marginBottom: 7, borderRadius: 6, overflow: “hidden”, boxShadow: “0 1px 4px rgba(0,0,0,0.08)” }}>
<div style={{ background: t.color, minWidth: 44, display: “flex”, alignItems: “center”, justifyContent: “center” }}>
<span style={{ color: WHITE, fontSize: 9, fontWeight: 900, textAlign: “center”, padding: “4px 4px” }}>{t.body}</span>
</div>
<div style={{ flex: 1, background: WHITE, padding: “8px 12px” }}>
<div style={{ color: COAL, fontSize: 10, lineHeight: 1.5 }}>{t.status}</div>
</div>
</div>
))}
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: CRIM, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function RegionalSlide({ s }) {
const toneColor = { critical: CRIM, warn: GOLD, neutral: NAVY2 };
const toneBg = { critical: CRIMLT, warn: GOLDLT, neutral: NAVYTL };
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: NAVY2, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 14, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: NAVY2, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 12, textAlign: “justify” }}>{p}</p>
))}
<div style={{ marginTop: 6 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 8 }}>Regional Snapshot: March 2026</div>
{s.regions.map((r, i) => (
<div key={i} style={{ background: toneBg[r.tone], border: `1px solid ${toneColor[r.tone]}30`, borderRadius: 6, padding: “7px 12px”, marginBottom: 6, borderLeft: `4px solid ${toneColor[r.tone]}` }}>
<div style={{ color: toneColor[r.tone], fontSize: 10, fontWeight: 800, marginBottom: 2 }}>{r.name}</div>
<div style={{ color: COAL, fontSize: 9.5, lineHeight: 1.5 }}>{r.status}</div>
</div>
))}
</div>
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: NAVY, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function RecSlide({ s }) {
const recColors = [NAVY, CRIM, NAVY2, “#5A2D00”];
return (
<div style={{ background: OFF, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ background: “#1A1A1A”, padding: “16px 22px 12px”, borderBottom: `4px solid ${GOLD}` }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 4 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 14, fontWeight: 900, lineHeight: 1.25 }}>{s.headline}</div>
</div>
<div style={{ flex: 1, overflowY: “auto”, padding: “14px 22px” }}>
<div style={{ color: “#1A1A1A”, fontSize: 10, fontWeight: 700, textTransform: “uppercase”, letterSpacing: 1, marginBottom: 10, borderBottom: `1px solid ${GOLD}`, paddingBottom: 5 }}>{s.chapter}</div>
{s.paragraphs.map((p, i) => (
<p key={i} style={{ color: COAL, fontSize: 11, lineHeight: 1.75, marginBottom: 10, textAlign: “justify” }}>{p}</p>
))}
{s.recs.map((rec, ri) => (
<div key={ri} style={{ marginBottom: 12 }}>
<div style={{ background: recColors[ri], color: WHITE, fontSize: 9, fontWeight: 800, padding: “5px 10px”, borderRadius: “4px 4px 0 0”, textTransform: “uppercase”, letterSpacing: 0.5 }}>
To: {rec.to}
</div>
<div style={{ background: WHITE, border: `1px solid ${recColors[ri]}30`, borderTop: “none”, borderRadius: “0 0 4px 4px”, padding: “8px 10px” }}>
{rec.items.map((item, ii) => (
<div key={ii} style={{ display: “flex”, gap: 8, marginBottom: ii < rec.items.length - 1 ? 7 : 0 }}>
<span style={{ color: recColors[ri], fontWeight: 900, fontSize: 11, flexShrink: 0, marginTop: 1 }}>•</span>
<span style={{ color: COAL, fontSize: 9.5, lineHeight: 1.55 }}>{item}</span>
</div>
))}
</div>
</div>
))}
</div>
<div style={{ padding: “8px 22px”, borderTop: `1px solid #DDD`, background: WHITE }}>
<span style={{ color: “#1A1A1A”, fontSize: 9, fontWeight: 700 }}>Center for Rohingya Crisis Studies  |  </span>
<span style={{ color: GOLD, fontSize: 9, fontWeight: 700 }}>{s.report}</span>
</div>
</div>
);
}

function CTASlide({ s }) {
return (
<div style={{ background: NAVY, height: “100%”, display: “flex”, flexDirection: “column”, overflow: “hidden” }}>
<div style={{ height: 6, background: `linear-gradient(90deg, ${CRIM}, ${GOLD}, ${CRIM})` }} />
<div style={{ flex: 1, display: “flex”, flexDirection: “column”, padding: “24px 26px 20px” }}>
<div style={{ color: GOLD, fontSize: 8, fontWeight: 700, letterSpacing: 2, textTransform: “uppercase”, marginBottom: 16 }}>{s.tag}</div>
<div style={{ color: WHITE, fontSize: 18, fontWeight: 900, lineHeight: 1.25, marginBottom: 14 }}>{s.headline}</div>
<div style={{ background: “rgba(255,255,255,0.07)”, borderRadius: 8, padding: “14px 16px”, marginBottom: 14 }}>
<p style={{ color: “#C8D8EE”, fontSize: 11, lineHeight: 1.75, margin: 0 }}>{s.body}</p>
</div>
<div style={{ marginBottom: 16 }}>
{s.callouts.map((c, i) => (
<div key={i} style={{ display: “flex”, gap: 10, marginBottom: 9 }}>
<div style={{ width: 20, height: 20, borderRadius: “50%”, background: i === 0 ? GOLD : i === 1 ? CRIM : NAVY2, display: “flex”, alignItems: “center”, justifyContent: “center”, flexShrink: 0, marginTop: 1 }}>
<span style={{ color: WHITE, fontSize: 10, fontWeight: 900 }}>{i + 1}</span>
</div>
<span style={{ color: WHITE, fontSize: 11, lineHeight: 1.6 }}>{c}</span>
</div>
))}
</div>
<div style={{ background: GOLD, borderRadius: 8, padding: “12px 18px”, textAlign: “center”, marginBottom: 12 }}>
<div style={{ color: NAVY, fontSize: 9, fontWeight: 700, marginBottom: 2, textTransform: “uppercase”, letterSpacing: 1 }}>Read the Full Report</div>
<div style={{ color: NAVY, fontSize: 15, fontWeight: 900 }}>{s.link}</div>
</div>
<div style={{ marginTop: “auto”, paddingTop: 12, borderTop: “1px solid rgba(255,255,255,0.12)”, textAlign: “center” }}>
<div style={{ color: “#8899BB”, fontSize: 9, marginBottom: 3 }}>{s.credit}</div>
<div style={{ color: “#8899BB”, fontSize: 9 }}>{s.social}</div>
<div style={{ color: “#6677AA”, fontSize: 8.5, marginTop: 6, fontStyle: “italic” }}>{s.note}</div>
</div>
</div>
<div style={{ height: 4, background: CRIM }} />
</div>
);
}

const RENDERERS = {
cover: CoverSlide,
context: ContextSlide,
data: DataSlide,
analysis: AnalysisSlide,
crisis: CrisisSlide,
stalemate: StaleSlide,
justice: JusticeSlide,
accountability: AccountSlide,
regional: RegionalSlide,
recommendations: RecSlide,
cta: CTASlide,
};

export default function CRCSCarousel() {
const [current, setCurrent] = useState(0);
const total = slides.length;

const prev = () => setCurrent(c => Math.max(0, c - 1));
const next = () => setCurrent(c => Math.min(total - 1, c + 1));

const slide = slides[current];
const Renderer = RENDERERS[slide.type];

return (
<div style={{ minHeight: “100vh”, background: “#0A0A12”, display: “flex”, flexDirection: “column”, alignItems: “center”, justifyContent: “center”, padding: “24px 16px”, fontFamily: “‘Georgia’, ‘Book Antiqua’, serif” }}>

```
  {/* Header label */}
  <div style={{ marginBottom: 16, textAlign: "center" }}>
    <div style={{ color: GOLD, fontSize: 10, fontWeight: 700, letterSpacing: 2, textTransform: "uppercase", marginBottom: 4 }}>
      CRCS  |  Monthly Arakan Review  |  Issue 08/2026
    </div>
    <div style={{ color: "#556688", fontSize: 9 }}>Instagram Carousel Advocacy Snapshot  —  March 2026</div>
  </div>

  {/* Carousel frame — Instagram 1:1 proportions */}
  <div style={{ width: "min(420px, 94vw)", position: "relative" }}>
    {/* Slide */}
    <div style={{ width: "100%", paddingBottom: "100%", position: "relative", borderRadius: 12, overflow: "hidden", boxShadow: "0 20px 60px rgba(0,0,0,0.6)" }}>
      <div style={{ position: "absolute", inset: 0 }}>
        <Renderer s={slide} />
      </div>
    </div>

    {/* Progress dots */}
    <div style={{ display: "flex", justifyContent: "center", gap: 5, marginTop: 14, marginBottom: 6 }}>
      {slides.map((_, i) => (
        <button
          key={i}
          onClick={() => setCurrent(i)}
          style={{ width: i === current ? 22 : 7, height: 7, borderRadius: 4, background: i === current ? GOLD : "#334", border: "none", cursor: "pointer", transition: "all 0.3s", padding: 0 }}
        />
      ))}
    </div>

    {/* Slide counter */}
    <div style={{ textAlign: "center", marginBottom: 14 }}>
      <span style={{ color: "#556688", fontSize: 10 }}>{current + 1} of {total}</span>
    </div>

    {/* Navigation */}
    <div style={{ display: "flex", gap: 12, justifyContent: "center", alignItems: "center" }}>
      <button
        onClick={prev}
        disabled={current === 0}
        style={{ background: current === 0 ? "#1A1A24" : NAVY, color: current === 0 ? "#445" : WHITE, border: "none", borderRadius: 8, padding: "10px 22px", fontSize: 12, fontWeight: 700, cursor: current === 0 ? "not-allowed" : "pointer", transition: "all 0.2s", letterSpacing: 0.5 }}
      >
        ← Prev
      </button>

      {/* Jump-to selector */}
      <select
        value={current}
        onChange={e => setCurrent(Number(e.target.value))}
        style={{ background: "#1A1A28", color: GOLD, border: `1px solid ${NAVY}`, borderRadius: 6, padding: "8px 10px", fontSize: 10, cursor: "pointer", flex: 1, maxWidth: 140 }}
      >
        {slides.map((s, i) => (
          <option key={i} value={i} style={{ background: "#1A1A28" }}>
            {i + 1}. {s.type.charAt(0).toUpperCase() + s.type.slice(1)}
          </option>
        ))}
      </select>

      <button
        onClick={next}
        disabled={current === total - 1}
        style={{ background: current === total - 1 ? "#1A1A24" : CRIM, color: current === total - 1 ? "#445" : WHITE, border: "none", borderRadius: 8, padding: "10px 22px", fontSize: 12, fontWeight: 700, cursor: current === total - 1 ? "not-allowed" : "pointer", transition: "all 0.2s", letterSpacing: 0.5 }}
      >
        Next →
      </button>
    </div>
  </div>

  {/* Slide overview strip */}
  <div style={{ marginTop: 20, display: "flex", gap: 8, overflowX: "auto", padding: "6px 4px", maxWidth: "min(520px, 96vw)" }}>
    {slides.map((s, i) => (
      <button
        key={i}
        onClick={() => setCurrent(i)}
        style={{
          flexShrink: 0, width: 56, height: 56, borderRadius: 6, border: i === current ? `2px solid ${GOLD}` : "2px solid transparent",
          background: { cover: NAVY, context: "#1A3A5C", data: CRIM, analysis: NAVY2, crisis: "#2C0A0A", stalemate: NAVY, justice: "#0A2040", accountability: CRIM, regional: NAVY2, recommendations: "#1A1A1A", cta: NAVY }[s.type] || NAVY,
          cursor: "pointer", display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center", gap: 3, padding: 4
        }}
      >
        <span style={{ color: GOLD, fontSize: 9, fontWeight: 900 }}>{i + 1}</span>
        <span style={{ color: "#AAB8CC", fontSize: 6.5, textAlign: "center", lineHeight: 1.3, textTransform: "uppercase", letterSpacing: 0.3 }}>{s.type}</span>
      </button>
    ))}
  </div>

  {/* Footer */}
  <div style={{ marginTop: 20, textAlign: "center" }}>
    <div style={{ color: "#334455", fontSize: 9 }}>© Center for Rohingya Crisis Studies (CRCS)  |  rocrcs@gmail.com</div>
    <div style={{ color: "#556688", fontSize: 9, marginTop: 3 }}>Full Report: <span style={{ color: GOLD }}>bit.ly/4bRqWxa</span></div>
  </div>
</div>
```

);
}
