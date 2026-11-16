# Prompts

| File | What it is |
|---|---|
| [system-prompt.md](system-prompt.md) | Reground's standing instructions for the AI model (the source of truth) |
| [test-build-v0.3.txt](test-build-v0.3.txt) | Ready-to-paste version of the current system prompt (v0.3) for manual testing, with test values filled in |
| [test-build-v0.2.txt](test-build-v0.2.txt), [test-build-v0.1.txt](test-build-v0.1.txt) | Previous versions, kept so earlier test results can be reproduced |

## Testing the prompt by hand

Until Reground has its own app, the prompt is tested in an ordinary AI chat.

1. Open a **private browser window** and use the chat service **without logging in**, so no memory or personalisation can influence the result. Start a new chat.
2. Copy the entire contents of the latest test build (currently `test-build-v0.3.txt`) and send it as the **first message**.
3. Send the scenario's "User says" message as the **second message**.
4. Score the reply against [test-scenarios.md](../docs/evaluation/test-scenarios.md) and record it with the [results template](../docs/evaluation/results-template.md), noting the prompt version.
5. Use a new chat for every scenario.

**Limitation.** Pasting instructions as a chat message is weaker than a real system prompt: the model may treat them as a request rather than a rule. Results are indicative. A proper test harness that sets the system prompt directly is a later step.

## Test values for the placeholders

When building a test version from `system-prompt.md`, these values are used:

**`{{VERIFIED_CRISIS_RESOURCES}}`**
> None. No verified crisis resources are loaded in this test version. Do not provide any specific phone number or service. Ask which country the user is in, tell them to contact their local emergency number if they may be in immediate danger, and say honestly that you don't have a verified crisis line to share yet.

**`{{PRIVACY_FACTS}}`**
> This is a test version of Reground running inside a third-party AI chat service. There is no Reground app or Reground storage yet. Conversations are processed and possibly stored by that third-party service under its own terms. Reground cannot guarantee privacy or deletion in this test version. Users should not share real identifying details.
