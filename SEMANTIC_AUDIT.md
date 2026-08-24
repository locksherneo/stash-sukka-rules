# Semantic Integrity Audit

Generator:

`Sukka List -> Stash V1.4.2.1 Semantic Integrity Bugfix Final`

## Global Rule Conservation

| Metric | Count |
|---|---:|
| Source files | 68 |
| Active files | 63 |
| Deprecated files | 5 |
| Source rules total | 378988 |
| Deprecated source rules | 77761 |
| Sukka Markers removed | 62 |
| iOS PROCESS rules filtered | 75 |
| Duplicates removed | 0 |
| Final output rules | 301090 |
| Unaccounted rules | 0 |

## Output

| Behavior | Providers | Rules |
|---|---:|---:|
| domain | 20 | 291257 |
| ipcidr | 11 | 5261 |
| classical | 26 | 4572 |

## Conservation Equation

```text
source_rules_total
=
deprecated_source_rules
+ markers_removed
+ ios_process_filtered
+ duplicates_removed
+ output_rules
```

```text
378988
=
77761
+ 62
+ 75
+ 0
+ 301090
```

## Result

```text
unaccounted_rules = 0
```

`0` means every source rule has been accounted for.
