<img src="https://raw.githubusercontent.com/sabaki-js/sabaki/main/assets/logo.svg" width="120" alt="sabaki logo" />

# @sabaki-js/agent-trace-observability

[![npm](https://img.shields.io/npm/v/%40sabaki-js%2Fagent-trace-observability)](https://www.npmjs.com/package/%40sabaki-js%2Fagent-trace-observability) [![license](https://img.shields.io/npm/l/%40sabaki-js%2Fagent-trace-observability)](https://github.com/sabaki-js/plugin-agent-trace-observability#readme) [![CI](https://github.com/sabaki-js/plugin-agent-trace-observability/actions/workflows/test-battery.yml/badge.svg)](https://github.com/sabaki-js/plugin-agent-trace-observability/actions)

AI agent trace decisions.

Questions: `needs_review` (0.59), `risk` (0.43), `action` (0.36), `outcome` (0.34), `urgency` (0.39). Weights: 48 KB.

## Usage

```ts
import { Sabaki } from "sabaki";
import plugin from "@sabaki-js/agent-trace-observability";

const sabaki = new Sabaki().register(plugin.default ?? plugin);
const r = sabaki.decide({ state: "..." });
// { domain: "agent_trace_observability", decision: ..., confidence: ..., plugin: "@sabaki-js/agent-trace-observability" }
```

Ask another question with `input.question`.

Part of [sabaki](https://github.com/sabaki-js/sabaki) — see the [GUIDE](https://github.com/sabaki-js/sabaki/blob/main/GUIDE.md).

## License

MIT
