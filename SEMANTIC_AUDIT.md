# Semantic Integrity Audit

Generator:

`Sukka List -> Stash V1.4.2.1 Semantic Integrity Bugfix Final`

## Global Rule Conservation

| Metric | Count |
|---|---:|
| Source files | 68 |
| Active files | 63 |
| Deprecated files | 5 |
| Source rules total | 378504 |
| Deprecated source rules | 77364 |
| Sukka Markers removed | 62 |
| iOS PROCESS rules filtered | 75 |
| Duplicates removed | 0 |
| Final output rules | 301003 |
| Unaccounted rules | 0 |

## Output

| Behavior | Providers | Rules |
|---|---:|---:|
| domain | 20 | 291174 |
| ipcidr | 11 | 5264 |
| classical | 26 | 4565 |

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
378504
=
77364
+ 62
+ 75
+ 0
+ 301003
```

## Result

```text
unaccounted_rules = 0
```

`0` means every source rule has been accounted for.
