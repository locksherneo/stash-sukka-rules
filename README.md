# Sukka List for Stash iOS

V1.5.1 preserves existing provider URLs while adding rule-by-rule optimized
Full and Lite profiles. Only reference one profile for a given source.

| Output | Compatibility | Behavior |
| --- | --- | --- |
| domain/, ipcidr/, classical/ | Existing V1.4.2.1 URLs | Legacy-compatible |
| ios/domain/, ios/ipcidr/ | New Full profile | Optimized domain and CIDR |
| ios/classical/ | New Full profile | Unsupported-for-promotion remainder |
| lite/ | iOS Lite profile | Omits only explicitly audited expensive rules |
| mrs/ios/, mrs/lite/ | Optional MRS mirrors | domain/ipcidr only |

Mihomo MRS files are Zstandard-compressed; their MRSv1 magic appears
inside the decompressed payload, not at the start of the binary file.

## Semantic guarantees

- Full profile conserves every non-marker, iOS-supported upstream rule.
- DOMAIN and DOMAIN-SUFFIX become domain providers.
- DOMAIN-WILDCARD remains classical because routing glob semantics
  are not equivalent to domain/MRS provider label wildcards.
- IP-CIDR and IP-CIDR6 become ipcidr providers.
- Mixed resolving/no-resolve CIDRs use separate provider files.
- DOMAIN-KEYWORD, DOMAIN-REGEX, ASN and other supported special rules
  remain in small classical providers.
- Existing root-level provider URLs retain their historical contents.
- Lite omissions are listed in IOS_LITE_OMISSIONS.json and
  IOS_LITE_OMITTED_RULES.txt; Full never silently discards those rules.

## Stash configuration

Start with STASH_PROVIDERS_FULL_MRS.yaml or
STASH_PROVIDERS_LITE_MRS.yaml when MRS is enabled; TEXT variants are
always available. Copy only the providers you actually reference.

Providers split from the same source must be adjacent and use the same
policy. Preserve the order in PROVIDER_MANIFEST.json. For example:

```yaml
rules:
  - RULE-SET,sukka-ios-non-ip-ai-domain,PROXY
  - RULE-SET,sukka-ios-non-ip-ai-classical,PROXY
```

Add no-resolve only to RULE-SET references whose ipcidr manifest
entry has no_resolve=true. Classical GEOIP/IP-ASN entries preserve
their inline no-resolve option.

On iOS, keep DNS upstreams to one or two and avoid loading both Full
and Lite or both legacy and optimized versions of the same rule set.
