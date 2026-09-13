# homebrew-agent-pet-runtime

Homebrew tap for [Agent Pet Runtime](https://github.com/dncore/agent-pet-runtime).

```bash
brew tap dncore/agent-pet-runtime
brew install --cask agent-pet-runtime
```

The cask is generated automatically by the release workflow in the main
repository whenever a `v*` tag is pushed. Edits here will be overwritten.

The app is ad-hoc signed rather than notarised. The cask strips the quarantine
attribute on install; if Gatekeeper still objects, see the caveats printed by
`brew info --cask agent-pet-runtime`.
