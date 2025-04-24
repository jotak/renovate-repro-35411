# 35411

## Current behavior

`go.mod` is modified with only the digest (without version), which breaks go.mod:

```
google.golang.org/genproto/googleapis/api 2d3770c4ea7f
```

e.g: https://github.com/netobserv/flowlogs-pipeline/pull/918/files#diff-33ef32bf6c23acb95f5902d7097b7a1d5128ca061167ec0716715b0b9eeaa5f6R147

## Expected behavior

Should be updated with the full version+digest:

```
google.golang.org/genproto/googleapis/api v0.0.0-20250422160041-2d3770c4ea7f
```

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/35411
