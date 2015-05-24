Here are the minutes from our meeting at LambdaConf 2015.

@michaelficarra @chexxor @andyarvanitis @benburdette

## Diamond Dependency Issues

- @chexxor presented the issue, see the https://github.com/chexxor/purescript-myexponent repository.
- `mysquare` and `mycube` depend on different versions of `myexponent` and `purescript-dep-management` depends on both `mysquare` and `mycube`.
- Bower gives a warning and requires the user to disambiguate the dependencies.
- It is necessary for someone to update `mysquare` and `mycube` to compatible dependency versions.
- Given that we use Git for dependencies, sending a PR or forking a repo is the recommended approach, although it admittedly involves some work.

## Documentation

- We should write a semver tutorial for beginners, specifically its use in PureScript and the way we rely on `~`-versions.

## Verified Semver

- Bower does what we need but doesn't enforce compatible versions of packages, merely warns. We should develop either a package manager or a Bower plugin or separate tool for enforcing semver versioning using the subtyping relationship at the module level.