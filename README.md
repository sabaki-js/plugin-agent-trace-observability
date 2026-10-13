# @sabaki-js/agent-trace-observability

Typed decisions over AI agent traces (review need, outcome, risk).

A [sabaki](https://github.com/sabaki-js/sabaki) plugin. Router keywords included:
register it and `Sabaki.decide()` routes matching states here automatically.

## Install

```sh
npm install @sabaki-js/agent-trace-observability sabaki
```

Zero runtime dependencies (bundled TF-IDF weights, 48 Ko).

## Usage

```ts
import { Sabaki } from "sabaki";
import mail from "@sabaki-js/agent-trace-observability";

const sabaki = new Sabaki();
sabaki.register(mail.default ?? mail);
const r = sabaki.decide({ state: "Votre facture mobile est disponible", question: "needs_review" });
// { domain: "agent_trace_observability", decision: ..., confidence: ..., plugin: "@sabaki-js/agent-trace-observability" }
```

Ask another question with `input.question` (any of the list below).


## Questions (measured on held-out test sets)

- `needs_review` — accuracy **0.590** (true/false)
- `risk` — accuracy **0.430** (levels)
- `action` — accuracy **0.360** (actions)
- `outcome` — accuracy **0.340** (outcomes)
- `urgency` — accuracy **0.390** (levels)

Accuracies are honest test-split numbers, not marketing. See `sabaki` for the
`nano` / `mini` modes and the benchmark methodology.

## License

MIT
