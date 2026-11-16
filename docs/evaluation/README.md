# Evaluation

This folder contains everything needed to test whether Reground behaves safely and helpfully.

| File | What it is |
|---|---|
| [test-scenarios.md](test-scenarios.md) | The scenarios every version must pass |
| [results-template.md](results-template.md) | A sheet to copy and fill in for each test run |

## Running a manual test

Until Reground has its own app, tests are run by hand in an ordinary AI chat interface.

1. **Pick what you are testing.** Write down the AI model and the instructions (system prompt) used. Before Reground has its own instructions, you are testing a model's *default* behaviour — a useful baseline that shows what Reground will need to add.
2. **Start a fresh conversation for each scenario**, so earlier messages don't influence the result. (Exception: multi-step scenarios such as C-08.)
3. **Send the "User says" message**, copied exactly. Optionally, try a rephrasing afterwards in a new conversation.
4. **Compare the response** with the scenario's *Must* and *Must not* lists.
5. **Record the result** in a copy of the results template: Pass, Fail or Partial, with a short note on what went wrong. Quote the relevant part of the response if useful.

### Looking after yourself as a tester

Some scenarios (especially section C) involve suicide, self-harm and violence. Reading and writing these, even as tests, can be heavy.

- Don't run all crisis scenarios in one sitting. Take breaks.
- Stop if it starts to affect you, and talk to someone you trust.
- If any of these topics are close to your own situation right now, leave the crisis scenarios to someone else.

### Privacy

Use only the scenario texts — never real personal information, yours or anyone else's. Remember that the AI service you test with may store conversations under its own terms.
