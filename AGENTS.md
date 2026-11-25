# lib-parse

The `parse` **port**: the `Parser`/`DynParser` traits and the
`parse.parse` op over a caller-supplied parser table
(`parse_op_registry_with`).

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the port surface |
| `pkg.hnl` | package manifest — `modules: ["parse"]` |
| `scripts/hnl-gate.sh`, `ci.sh` | the gate / bupha entry |

## Contract

- Rule B: this crate knows **no parsers** — `lib-url-rfc` /
  `lib-url-whatwg` register themselves into the caller-supplied
  parser table.
- No Rust crate in this repo; the traits/op are the port contract.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
