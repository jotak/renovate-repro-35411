# 35411

## Current behavior

Failing to update a go module from version+digest to newer version (which is without digest: v0.5.10).
See in [renovate.log](./renovate.log) :

```json
                 "updates": [],
                 "packageName": "github.com/safchain/ethtool",
                 "warnings": [
                   {
                     "message": "Could not determine new digest for update (go package github.com/safchain/ethtool)",
                     "topic": "github.com/safchain/ethtool"
                   }
                 ]
```

I'm running:

```bash
LOG_LEVEL=debug npx --package renovate -- renovate --platform=local
```

## Expected behavior

Since versions without digest is very common in go, the update should work and not complain about missing digest.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/35411
