# Cosmos SDK v0.45.13-classic Release Notes

This release introduces one bug fix, namely [#14798](https://github.com/cosmos/cosmos-sdk/pull/14798) and a bump to Tendermint v0.34.26, as per its [security advisory](https://github.com/informalsystems/tendermint/security/advisories/GHSA-cpqw-5g6w-h8rr).

**NOTE**: Add or update the following replace in the `go.mod` of your application:

```go
// use informal system fork of tendermint
replace github.com/tendermint/tendermint => github.com/informalsystems/tendermint v0.34.26
```

Please see the [CHANGELOG](https://github.com/cosmos/cosmos-sdk/blob/release/v0.45.x/CHANGELOG.md) for an exhaustive list of changes.

**Full Commit History**: https://github.com/classic-terra/cosmos-sdk/compare/v0.44.6-classic...v0.45.13-classic

**NOTE:** The changes mentioned in `v0.45.9` are **no longer required**. The following replace directive can be removed from the chains.

```go
# Can be deleted from go.mod
replace github.com/confio/ics23/go => github.com/cosmos/cosmos-sdk/ics23/go v0.8.0
```

Instead, `github.com/confio/ics23/go` must be **bumped to `v0.9.0`**.
