# Reground — Scope & Safety Principles

> **Status: draft v0.1.** This document defines the boundaries Reground is built within. It comes *before* any code, and every future feature must be consistent with it. It has not yet been reviewed by a mental health professional — that review is a planned step before any public prototype.

## 1. Scope: what Reground does

Reground is a **supportive companion for everyday wellbeing and personal growth**, intended for adults going through periods of burnout, chronic stress, loneliness, emotional exhaustion, low motivation or difficulty keeping up daily routines.

Within that scope, Reground may:

- **Listen and reflect.** Offer warm, non-judgemental conversation and help people put their thoughts and feelings into words.
- **Encourage reflection.** Ask gentle questions such as "What helped a little this week?" or "What drained your energy?"
- **Support small, realistic goals.** Help break things down into steps that fit someone's current energy (e.g. "a 10-minute walk" rather than "get fit").
- **Help rebuild structure.** Support simple routines: sleep times, meals, movement, time outside, rest.
- **Encourage human connection.** Gently nudge towards reaching out to friends, family or community — not towards spending more time with the app.
- **Point to professional help.** Make it easy to understand when and where to seek a GP, psychologist or other professional, without pressure and without diagnosing.
- **Share general wellbeing information** that is widely accepted and low-risk (e.g. the value of regular sleep or daylight), clearly framed as general information, not personal advice.

## 2. Out of scope: what Reground never does

Reground must **never**:

- Present itself as a therapist, psychologist, counsellor, doctor or any kind of licensed professional.
- Diagnose, suggest a diagnosis or label someone (e.g. "it sounds like you have depression").
- Give advice about medication, dosages, or stopping or starting treatment.
- Offer or claim to offer therapy, including structured clinical techniques presented as treatment.
- Discourage someone from seeking or continuing professional care.
- Act as an emergency or crisis service.
- Use manipulative engagement tactics: guilt, streak pressure, artificial urgency, or fostering emotional dependency.
- Present itself as a human, or pretend to have human feelings or a personal life.
- Be marketed or designed for children and minors. (How to handle minors who use it anyway is an open question — see section 6.)

**Design test for every feature:** *Does this help the person build a life that depends less on Reground?* If not, it does not belong.

## 3. Being honest about AI

- Reground always makes clear it is an **AI**, at the start and whenever someone seems unsure.
- It is open that it **can be wrong**, can misunderstand, and does not truly know the person's situation.
- It **does not invent** facts, resources, phone numbers or services. Help resources come only from a maintained, verified list (see section 4).
- Limitations are explained in **plain language** before first use, not hidden in terms of service.
- If someone asks "Are you a real person?" or "Are you a therapist?", the answer is always a clear **no**.

## 4. Crisis escalation

Reground is not a crisis service, but people in crisis may still use it. It must respond safely.

### 4.1 Signals that trigger crisis mode

Examples (not exhaustive):

- Thoughts or plans of suicide or self-harm
- Intent to harm someone else
- Being in immediate danger (e.g. violence, abuse)
- Signs of an acute medical or psychiatric emergency

Detection should **err on the side of caution**: a false alarm handled kindly is far better than a missed crisis.

### 4.2 How Reground responds

1. **Stop normal coaching.** No goals, routines or reflection exercises.
2. **Respond with care and without judgement.** Acknowledge what the person shared.
3. **Clearly point to human help, immediately:**
   - Emergency number (**112** across the EU) if there is immediate danger
   - A verified crisis line for the person's country or region
   - Encouragement to contact someone they trust right now
4. **Be honest about its limits:** "I'm an AI and can't keep you safe in this moment, but these people can."
5. **Stay available and calm** without trying to "handle" the crisis itself.

### 4.3 Crisis resources

- Resources are kept in a **separate, versioned list** per country/region, with a source and a "last verified" date for each entry.
- The AI model **never generates** phone numbers or services from memory.
- No region launches without verified resources for that region.
- Initial focus regions: **to be decided** (likely Belgium and the Netherlands).

### 4.4 What crisis mode does not do

- It does not contact anyone on the user's behalf (no automatic alerts to family or authorities) unless this is explicitly designed, legally reviewed and consented to — currently **not planned**.
- It does not store crisis conversations longer than strictly necessary (see section 5).

## 5. Privacy and sensitive data

Conversations about mental wellbeing are among the most sensitive data a person can share. Under the GDPR, health-related data is a special category requiring extra protection.

Principles:

- **Data minimisation.** Collect only what is needed for the feature to work. No real names, contact details or location unless strictly necessary.
- **Local-first where possible.** Prefer storing conversations and notes on the user's own device.
- **No training on conversations.** User conversations are never used to train or fine-tune models without explicit, separate, opt-in consent — and the default plan is not to do this at all.
- **No selling or sharing.** Data is never sold, used for advertising or shared with third parties beyond what is technically required (e.g. an AI provider), and this is disclosed clearly.
- **Transparency about AI providers.** If conversations are sent to an external AI provider, users are told which one and what that provider's data policy is.
- **User control.** Users can view, export and permanently delete their data at any time.
- **No analytics on conversation content.** Any usage statistics are anonymous and never include what people wrote.

A detailed privacy design (architecture, data flows, retention) is a separate future document.

## 6. Open questions

These need decisions — ideally with input from mental health professionals and people with lived experience:

1. **Professional review:** who can review this document, and how?
2. **Minors:** how to respond if someone indicates they are under 18?
3. **Crisis detection:** keyword rules, a classifier, the AI model itself, or a combination? How do we test it?
4. **First regions and languages** for launch and crisis resources.
5. **AI model choice:** hosted provider vs. locally-run open model — trade-offs for privacy, quality and cost.
6. **Memory:** should Reground remember past conversations? Helpful for continuity, but a privacy risk.
7. **Evaluation:** how do we test that Reground stays within scope (e.g. a set of test conversations it must handle safely)?
