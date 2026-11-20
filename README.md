# lib-parse

The `parse` port: the `Parser`/`DynParser` traits and the `parse.parse` op
over a caller-supplied parser table (`parse_op_registry_with`).

Rule B: this crate knows no parsers; `lib-url-rfc` / `lib-url-whatwg` register
themselves.

## Layout

```text
src/index.hnl   the .hnl sources
pkg.hnl         package manifest — modules, deps, description, license
ci.sh           bupha entry → scripts/hnl-gate.sh
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
