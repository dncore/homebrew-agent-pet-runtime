# homebrew-agent-pet-runtime

Homebrew tap for [Agent Pet Runtime](https://github.com/dncore/agent-pet-runtime).

```bash
brew tap dncore/agent-pet-runtime
brew install --cask dncore/agent-pet-runtime/agent-pet-runtime
```

The name is spelled in full because Homebrew treats a third-party tap as
untrusted until it is told otherwise, and refuses to load a cask out of one:
`brew install --cask agent-pet-runtime` stops with `Refusing to load cask …
from untrusted tap …`. Asking for `tap/name` trusts that one cask, which is the
shorter path; `brew trust dncore/agent-pet-runtime` does the same for the whole
tap.

The cask is generated automatically by the release workflow in the main
repository whenever a `v*` tag is pushed. Edits here will be overwritten.

The app is ad-hoc signed rather than notarised, so a copy macOS quarantined —
downloaded through a browser, or dragged out of the zip in Finder — is reported
by Gatekeeper as damaged. A `brew install` is not quarantined in the first
place, and the cask no longer strips anything on install; if a copy still
objects, `brew info --cask agent-pet-runtime` prints the one-line fix.
