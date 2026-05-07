# PDFluent

**Pure-Rust PDF SDK** — text extraction, forms, PDF/A, digital signatures, redaction, and WASM.

A modern alternative to iText, Apryse, and PDFBox. No JVM. No C++. No "Contact Sales" pricing.

## Get started

```toml
# Cargo.toml
[dependencies]
pdfluent = "1.0.0-beta.5"
```

```rust
use pdfluent::prelude::*;

let doc = PdfDocument::open("input.pdf")?;
println!("{}", doc.extract_text()?);
```

## Quick links

| | |
|---|---|
| Crate | [`pdfluent`](https://crates.io/crates/pdfluent) on crates.io |
| Docs | [pdfluent.com/docs](https://pdfluent.com/docs) |
| Examples | [`pdfluent/examples`](https://github.com/pdfluent/examples) — Rust, Node.js, Python, WASM |
| Pricing | [pdfluent.com/pricing](https://pdfluent.com/pricing) — Lite → Unlimited → Enterprise |
| Trial | [pdfluent.com/trial](https://pdfluent.com/trial) — 30-day license key |
| Changelog | [pdfluent.com/changelog](https://pdfluent.com/changelog) |

## Capabilities

| Feature | Status |
|---|---|
| Text extraction | Production |
| AcroForm fill + flatten | Production |
| Digital signatures (PAdES B-LT/B-LTA) | Production |
| PDF/A validation + conversion | Production |
| Content redaction | Production |
| WASM target | Production |
| Node.js native bindings | Production |
| Python wheels | Production |
| XFA form flattening | Beta |

---

Built by [Innovation Trigger BV](https://pdfluent.com) · [pdfluent.com](https://pdfluent.com)
