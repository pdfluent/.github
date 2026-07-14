# PDFluent

Two things: a free, source-available PDF editor for macOS and Windows, and a pure-Rust PDF SDK with bindings for six languages. Both are built on the same engine, no Pdfium, Poppler, MuPDF, or other C/C++ dependency underneath.

## The editor

Free for everyone, including commercial use. No account, no upload, no subscription.

- [Download for macOS and Windows](https://pdfluent.com/download)
- [Source (source-available, not open source)](https://github.com/pdfluent/pdfluent)
- [pdfluent.com](https://pdfluent.com)

## The SDK

A modern alternative to iText, Apryse, and PDFBox for developers building their own PDF tooling. The core engine has no JVM or C++ dependency; if you use the Java binding, that binding itself is native, not a JVM reimplementation of the engine.

```toml
# Cargo.toml
[dependencies]
pdfluent = "1.0.0-beta.17"
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
| Digital signatures (PAdES B-LT/B-LTA) | Production |
| PDF/A validation and conversion | Production |
| Content redaction | Production |
| XFA form flattening | Beta |

### Quick links

| | |
|---|---|
| Documentation | [pdfluent.com/docs](https://pdfluent.com/docs) |
| Examples | [`pdfluent/examples`](https://github.com/pdfluent/examples): Rust, Python, Node.js, WASM |
| SDK pricing | [pdfluent.com/sdk/pricing](https://pdfluent.com/sdk/pricing) |
| Trial | [pdfluent.com/trial](https://pdfluent.com/trial): 30-day license key |
| Changelog | [pdfluent.com/changelog](https://pdfluent.com/changelog) |

---

Built by [Innovation Trigger BV](https://pdfluent.com). [pdfluent.com](https://pdfluent.com)
