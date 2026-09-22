# PDFluent

Two things: a free, source-available PDF editor for macOS and Windows, and a pure-Rust PDF SDK with bindings for six languages. Both are built on the same engine, no Pdfium, Poppler, MuPDF, or other C/C++ dependency underneath.

## The editor

Free for everyone, including commercial use. No account, no upload, no subscription.

- [Download for macOS and Windows](https://pdfluent.com/download)
- [Source (source-available, not open source)](https://github.com/pdfluent/pdfluent)
- [pdfluent.com](https://pdfluent.com)

## The SDK

AGPL-3.0, and the free build is the complete product: no licence key, no activation call, no tier, every feature in every build. If you cannot accept the copyleft obligation, a commercial licence is sold yearly and self-service — Commercial per organisation, OEM Startup and OEM per product, and Priority support as an add-on.

A modern alternative to iText, Apryse, and PDFBox for developers building their own PDF tooling. The core engine has no JVM or C++ dependency; if you use the Java binding, that binding itself is native, not a JVM reimplementation of the engine.

```toml
# Cargo.toml
[dependencies]
pdfluent = "1.0.0"
```

```rust
use pdfluent::prelude::*;

let doc = PdfDocument::open("input.pdf")?;
println!("{}", doc.extract_text()?);
```

### Language bindings

| Language | Package |
|---|---|
| Rust | [`pdfluent`](https://crates.io/crates/pdfluent) on crates.io |
| Python | [`pdfluent`](https://pypi.org/project/pdfluent) on PyPI |
| Node.js | [`@pdfluent/node`](https://www.npmjs.com/package/@pdfluent/node) on npm |
| Browser / WASM | [`@pdfluent/sdk-wasm`](https://www.npmjs.com/package/@pdfluent/sdk-wasm) on npm |
| .NET | [`pdfluent`](https://www.nuget.org/packages/pdfluent) on NuGet |
| Java | [`com.pdfluent:pdfluent`](https://central.sonatype.com/artifact/com.pdfluent/pdfluent) on Maven Central |

### Capabilities

| Feature | Status |
|---|---|
| Text extraction | Production |
| AcroForm fill and flatten | Production |
| Digital signatures (PAdES B-B / B-T / B-LT) | Production |
| PDF/A validation and conversion | Production |
| Content redaction | Production |
| XFA form flattening | Beta |

### Quick links

| | |
|---|---|
| Documentation | [pdfluent.com/docs](https://pdfluent.com/docs) |
| SDK source | [`pdfluent/pdfluent-sdk`](https://github.com/pdfluent/pdfluent-sdk) |
| Examples | [`pdfluent/examples`](https://github.com/pdfluent/examples): Rust, Python, Node.js, WASM |
| SDK licence | AGPL-3.0, or a commercial licence sold yearly and self-service at [pdfluent.com/sdk/pricing](https://pdfluent.com/sdk/pricing) |
| Changelog | [pdfluent.com/changelog](https://pdfluent.com/changelog) |

The PDF rendering path builds on [`hayro`](https://github.com/pdfluent/hayro),
Laurenz Stampfl's pure-Rust PDF interpreter — mirrored here and credited
upstream in `pdfluent-sdk`'s own README.

## Also available on

- [Microsoft Store](https://apps.microsoft.com/detail/xpdbxj6xrlfqk2) — the editor, for Windows

## Repositories

| Repository | What's in it |
|---|---|
| [`pdfluent/pdfluent`](https://github.com/pdfluent/pdfluent) | The desktop editor (Tauri + React/TypeScript). Source-available. |
| [`pdfluent/pdfluent-sdk`](https://github.com/pdfluent/pdfluent-sdk) | The PDF SDK itself — pure-Rust engine plus the Python, Node.js, .NET, Java, C, and WASM bindings. AGPL-3.0 or commercial. |
| [`pdfluent/examples`](https://github.com/pdfluent/examples) | Runnable SDK examples in Rust, Python, Node.js, and a browser/WASM demo. |
| [`pdfluent/hayro`](https://github.com/pdfluent/hayro) | Mirror of the upstream PDF interpreter the rendering path is built on. |
| [`pdfluent/.github`](https://github.com/pdfluent/.github) | This profile, plus shared issue templates, contributing guide, and security policy. |

---

Built by [Innovation Trigger BV](https://pdfluent.com). [pdfluent.com](https://pdfluent.com)
