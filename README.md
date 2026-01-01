## zavisimost-konec

Binary / third‑party dependencies used by TDS projects (for example `spina-konec`).

### Repository structure

- **Git repo**: Contains only lightweight metadata (this README, maybe small index files).
- **GitHub Releases**: Actual binary artifacts are stored as **release assets**, not committed to Git.

### Current bundles

- **decklink-14.1**
  - `Blackmagic_DeckLink_SDK_14.1.zip`
  - `Blackmagic_Desktop_Video_Linux_14.1.tar` (or `.tar.tar`, depending on vendor package)

### How other projects should use this repo

Other repos (like `spina-konec`) should reference **release asset URLs**, for example:

```bash
CLOUD_SDK_URL="https://github.com/<user-or-org>/zavisimost-konec/releases/download/decklink-14.1/Blackmagic_DeckLink_SDK_14.1.zip"
CLOUD_DRIVER_URL="https://github.com/<user-or-org>/zavisimost-konec/releases/download/decklink-14.1/Blackmagic_Desktop_Video_Linux_14.1.tar"
```

These URLs are suitable for non-interactive tools like `curl` or `wget` and can be plugged directly into setup scripts.

> **Note**: These binaries are third‑party artifacts (e.g., Blackmagic DeckLink SDK & drivers). Make sure you comply with the vendor’s licensing terms when downloading or redistributing them.

