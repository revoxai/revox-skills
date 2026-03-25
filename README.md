# Revox Skills Library

> Ready-to-use prompt templates for AI voice agents — extracted from real production agents.

---

## Available Skills

| Skill | Folder | Languages | Use cases |
|---|---|---|---|
| 💰 Debt Collection | [debt-collection/](./debt-collection/SKILL.md) | FR, EN | Invoice recovery, failed payments, instalment plans |
| 📋 Survey | [survey/](./survey/SKILL.md) | FR, EN | Market research, brand perception, CSAT, NPS |
| 📞 Cold Calling / SDR | [cold-calling-sdr/](./cold-calling-sdr/SKILL.md) | FR, EN | Outbound prospecting, event invitations, demos |
| 📅 Appointment Booking | [appointment-booking/](./appointment-booking/SKILL.md) | FR, EN | Confirmations, reminders, rescheduling |
| 👥 Staffing & Recruitment | [staffing-recruitment/](./staffing-recruitment/SKILL.md) | FR, EN | Pre-qualification, interviews, document collection |
| 🎯 Lead Qualification | [lead-qualification/](./lead-qualification/SKILL.md) | FR, EN | BANT qualification, inbound follow-up, lead scoring |
| 🚀 Onboarding & Support | [onboarding-support/](./onboarding-support/SKILL.md) | FR, EN, DE, IT | User activation, setup guidance, inbound support |

---

## How to use a skill

Each `SKILL.md` file contains:

1. **Core prompt template** — copy, fill in the variables, and paste into your agent's prompt field
2. **Variable definitions** — what to pass in `prompt_variables`
3. **Recommended first sentence** — paste into `first_sentence` field
4. **Structured output config** — paste into `structured_output_config` (JSON)
5. **Best practices** — do's, don'ts, and objection handling
6. **Production-tested use cases** — real scenarios for inspiration

---

## Universal Rules (apply to all skills)

These rules should be included in every agent prompt:

```
# Universal voice agent rules
- Stay concise — max 60 tokens per turn. One question at a time.
- Your output goes to text-to-speech. Use naturally pronounceable words and sentences.
- If asked whether you are an AI → always confirm it clearly and honestly.
- If the person wants to stop → thank them and end the call immediately.
- Rephrase unclear questions once, then accept the answer and move on.
- For EU/French calls: inform that the call is recorded at the start.
```

---

## Variable Syntax

Use double curly braces for all dynamic variables:

```
{{variable_name}}
```

Pass values in `prompt_variables`:
```json
{
  "agent_name": "Lucie",
  "company_name": "YourCompany",
  "contact_name": "Marie"
}
```
