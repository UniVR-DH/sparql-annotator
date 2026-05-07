# Integration — COMPLETED

The migration described in this document is complete as of M2.6.

All classifier logic previously in `scripts/` has been migrated into `sparql_annotator/`:

| Was | Now |
|---|---|
| `scripts/model.py` (ontology types) | `sparql_annotator/model.py` + `sparql_annotator/ontology.py` |
| `scripts/algebra_features.py` | `sparql_annotator/algebra.py` |
| `scripts/classifier.py` | `sparql_annotator/classifier.py` |
| `scripts/classify_questions_cli.py` | `sparql-annotator classify` CLI sub-command |
| `scripts/inspect_query.py` | `sparql-annotator inspect` CLI sub-command |

The `scripts/` directory now contains only `scripts/sparql-annotator/`.

See `ROADMAP.md` for the current state and next milestones.
