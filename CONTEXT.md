# GuideSite

GuideSite is the cross-industry domain language for an AI-first decision website that helps visitors decide whether an offer fits their situation. This glossary keeps product, ethics, and content terms stable as the system grows.

## Language

**GuideSite**:
An intent-first website experience where the visitor’s goal shapes the interface in real time. It is the primary homepage decision experience, not a conventional website with a chatbot attached.
_Avoid_: Website with chatbot, chatbot website, AI homepage, RAG site

**Decision Journey**:
The visitor’s path from an unresolved question or concern to a clearer decision about an offer. The journey may end in action, deferral, or a conclusion that the offer is not a fit.
_Avoid_: Funnel, conversion flow, sales script

**Offer**:
The product, service, program, or opportunity being evaluated inside a GuideSite. The offer is what the visitor is deciding about, not the GuideSite itself.
_Avoid_: SKU, campaign, asset

**Fit Assessment**:
The central user-facing evaluation of whether an offer suits the visitor’s situation, constraints, needs, and preferences. A fit assessment can produce a Fit Outcome, Partial Fit Outcome, No-Fit Outcome, or an internal Information Gap that leads to a Clarifying Question.
_Avoid_: Lead qualification, sales qualification, conversion scoring

**Approved Content**:
Information the represented company has accepted as safe to use when helping visitors understand an offer. Approved content includes both tightly structured content and loosely structured content.
_Avoid_: Random chunks, scraped content, model knowledge

**Tightly Structured Content**:
Approved Content captured in strict typed fields, such as facts, values, rules, dates, prices, schedules, packages, availability, or eligibility details. Tightly structured content is useful when the visitor needs exact facts or the Fit Assessment needs firm boundaries.
_Avoid_: Hardcoded rule, backend config, hidden logic

**Loosely Structured Content**:
Approved Content captured in flexible rich text, such as policies, guides, FAQs, explanations, proof, and trust-building material. Loosely structured content is useful when the visitor needs context, nuance, or education.
_Avoid_: Unstructured content, narrative content, prose blob

**Evidence-Backed Answer**:
An answer that traces important claims back to approved content and shows the relevant evidence to the visitor. It should make uncertainty visible instead of filling gaps with persuasion.
_Avoid_: Sales copy, model opinion, unsupported answer

**Evidence**:
Approved Content shown to support the current answer, Fit Assessment, recommendation, caveat, or no-fit reasoning. Evidence should appear in the GuideSite Session through the appropriate Static Generative UI components.
_Avoid_: Hidden citation, internal source, decorative proof

**Guided Decision Environment**:
A website experience that combines conversation, structured explanations, proof, tools, and next steps around the visitor’s actual goal. It is broader than chat and narrower than an open-ended assistant.
_Avoid_: Chatbot, generic AI assistant, brochure site

**Visitor**:
The person using a GuideSite to understand an offer and decide whether it fits their situation. A visitor is not a lead unless they consent to continue with the represented company.
_Avoid_: User, prospect, lead

**Lead**:
A business record for a visitor who has consented to handoff, follow-up, or another explicit next step with the represented company. A lead is an outcome of consent, not the default identity of every visitor.
_Avoid_: Visitor, user, traffic

**Customer**:
A person or organization that has bought, enrolled in, or otherwise accepted the offer. A customer is not the same thing as a visitor who is still deciding.
_Avoid_: Visitor, lead, user

**Represented Company**:
The organization whose offer is being explained and evaluated inside a GuideSite. The GuideSite may represent the company, but the visitor’s decision remains the primary concern.
_Avoid_: Client, business, provider, account

**High-Stakes Decision Market**:
A market where choosing badly can cost the visitor significant money, time, safety, trust, or emotional effort. GuideSite is built for these markets because visitors need evidence and judgment, not just promotion.
_Avoid_: High-ticket market, considered purchase market, complex service market

**Fit Rule**:
A hard requirement, exclusion, or caveat captured as Approved Content that can determine whether an offer is available or appropriate for a visitor. Fit rules should not be softened into persuasive suggestions.
_Avoid_: Sales rule, lead score, preference

**Practical Fit**:
How well an offer matches the visitor’s concrete constraints, such as timing, budget, logistics, support needs, risk, or readiness. Practical fit can block an otherwise attractive offer.
_Avoid_: Convenience, nice-to-have, qualification

**Preference Fit**:
How well an offer matches the visitor’s goals, values, comfort level, style, and tradeoffs. Preference fit helps choose among viable options but should not override hard fit rules.
_Avoid_: Vibe, taste, upsell angle

**Fit Outcome**:
A Fit Assessment result where the offer appears to suit the visitor’s stated situation, constraints, needs, and preferences. A fit outcome should still show the evidence and caveats behind the conclusion.
_Avoid_: Qualified lead, conversion-ready, green light

**Partial Fit Outcome**:
A Fit Assessment result where the offer may suit the visitor, but only with meaningful caveats, tradeoffs, missing constraints, or unresolved concerns. A partial fit outcome should help the visitor understand what would need to be true for the offer to make sense.
_Avoid_: Maybe, soft yes, objection

**No-Fit Outcome**:
A Fit Assessment result where the offer does not suit the visitor’s stated situation, constraints, needs, or preferences. A no-fit outcome should explain why, point to neutral next steps, and avoid Consented Handoff unless the case needs human review.
_Avoid_: Failed lead, disqualified prospect, rejection

**Neutral Next Step**:
Helpful guidance after fit, partial fit, no fit, or uncertainty that does not pressure the visitor toward the represented company. Neutral next steps should stay within the represented company’s offer unless outside alternatives are explicitly approved later.
_Avoid_: Sales CTA, conversion prompt, objection close, competitor recommendation

**Information Gap**:
An internal conclusion that the GuideSite is missing required visitor context for the current decision. An information gap should become a targeted question, not a final user-facing result.
_Avoid_: Unknown, low confidence, incomplete assessment

**Clarifying Question**:
A user-facing question that asks for the most important missing information needed to continue the visitor’s Decision Journey. A clarifying question should ask the blocking question first and should not collect data for its own sake.
_Avoid_: Form field, qualification question, data capture

**Content Gap**:
An internal conclusion that the GuideSite lacks approved content needed to answer or assess a company-specific question. A content gap should be stated as something the GuideSite cannot verify, not filled with general knowledge.
_Avoid_: Guess, fallback answer, hallucination

**Consent Boundary**:
The line between using visitor information to help with the current conversation and retaining, analyzing, or sharing it beyond that conversation. Crossing the consent boundary requires explicit visitor permission.
_Avoid_: Implied consent, hidden tracking, automatic lead capture

**GuideSite Session**:
One visitor’s active interaction with a GuideSite, including the conversation, gathered context, displayed interface, and current Fit Assessment state. A GuideSite Session is bounded by the Consent Boundary for any retention, analytics, or handoff.
_Avoid_: Chat thread, visit, funnel session

**GuideSite Turn**:
One exchange inside a GuideSite Session where the visitor provides input and the GuideSite responds with guidance, questions, content, interface, or next steps. A GuideSite Turn should advance the Decision Journey, not merely generate a reply.
_Avoid_: Bot reply, agent run

**Static Generative UI**:
A GuideSite interface model where every visual component is predefined, but each GuideSite Turn can assemble a different combination of those components. The AI may choose and populate approved components, but it does not invent new components, layouts, styles, or interaction patterns.
_Avoid_: Arbitrary generated UI, AI-generated markup, chatbot skin

**Chat**:
The main GuideSite surface where visitor messages, GuideSite responses, and Static Generative UI appear in a threaded exchange. Chat is the surface of the experience, not the whole value of the GuideSite.
_Avoid_: Threaded interaction surface, chatbot box

**Visitor Goal**:
What the visitor is trying to figure out, decide, compare, understand, or do in a GuideSite Session. The Visitor Goal should shape the answer, questions, content, UI, and next steps in each GuideSite Turn.
_Avoid_: Intent, query, prompt, traffic objective

**Visitor Context**:
Information the visitor shares to help the GuideSite understand their situation, constraints, preferences, worries, goals, or decision criteria. Visitor Context belongs inside the GuideSite Session unless the visitor consents to retention, analytics, or handoff.
_Avoid_: Lead data, customer data, profile

**Consented Handoff**:
The moment when a visitor gives clear permission to continue with the represented company, such as follow-up, booking, enrollment, application, or another explicit next step. A consented handoff is when Visitor Context may become Lead information.
_Avoid_: Lead conversion, capture, automatic handoff

**Offer Question**:
A visitor question about the represented company’s offer, such as features, policies, schedules, pricing, procedures, availability, or proof. Offer questions should be answered from Approved Content.
_Avoid_: FAQ, product question, sales question

**Learning Question**:
A visitor question about the broader decision domain, not only the represented company’s offer. Learning questions should use Approved Content first; general domain guidance is allowed only when it is clearly labeled as general.
_Avoid_: Education content, blog topic, generic explainer

**Fit Question**:
A visitor question about whether the offer suits their own situation, needs, constraints, preferences, or goals. Fit questions usually require both Approved Content and Visitor Context.
_Avoid_: Subjective question, lead qualification, recommendation prompt

**General Guidance**:
Educational help about a high-stakes decision domain that is not specific to the represented company’s offer. General guidance must be labeled clearly so visitors do not confuse it with Approved Content.
_Avoid_: Company claim, verified offer fact, hidden source

**Session Timeline**:
The ordered stream of chat messages, answers, evidence, questions, and Static Generative UI components created during a GuideSite Session. The Session Timeline is page-like for the visitor, but it is not the same as a normal website page.
_Avoid_: Session page, generated page, chatbot transcript

**Authorized Editor**:
A person at the represented company who is allowed to create, edit, or approve Approved Content. Authorized Editors help keep GuideSite answers grounded in company-approved information.
_Avoid_: Admin, content steward, business user

**Fit-First Principle**:
The rule that a GuideSite should help the visitor understand objective fit before trying to create a lead, sale, enrollment, application, or other business outcome. The visitor makes the decision; the GuideSite helps them see whether the offer fits.
_Avoid_: Conversion-first, sales-first, persuasion-first

**Fit Recommendation**:
A suggested offer option based on Visitor Context, Approved Content, Evidence, and the current Fit Assessment. A Fit Recommendation should explain why the option fits and what caveats remain.
_Avoid_: Upsell, product match, sales recommendation

**Objective Fit**:
Fit based on Visitor Context, Approved Content, Evidence, and Fit Rules, while making unknowns and caveats visible. Objective fit is evidence-based, not mathematically certain.
_Avoid_: Ideal customer profile, gut feel, guaranteed fit

**Visitor Concern**:
A worry, hesitation, risk question, objection, or uncertainty the visitor brings into a GuideSite Session. A Visitor Concern should be addressed with evidence, plain explanation, and fit-aware guidance rather than pressure.
_Avoid_: Objection, barrier, sales resistance
