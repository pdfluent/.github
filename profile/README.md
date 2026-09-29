<p align="center">
  <a href="https://pdfluent.com/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=logo">
    <img src="https://pdfluent.com/favicon.svg" width="72" alt="PDFluent logo"/>
  </a>
</p>

<h1 align="center">PDFluent</h1>

<p align="center"><strong>A PDF editor and a PDF SDK on one Rust engine.</strong></p>

<p align="center">
  <a href="https://crates.io/crates/pdfluent"><img src="https://img.shields.io/crates/v/pdfluent?label=crates.io&color=111111" alt="crates.io"/></a>
  <a href="https://pypi.org/project/pdfluent/"><img src="https://img.shields.io/pypi/v/pdfluent?label=PyPI&color=111111" alt="PyPI"/></a>
  <a href="https://www.npmjs.com/package/@pdfluent/node"><img src="https://img.shields.io/npm/v/%40pdfluent%2Fnode?label=npm&color=111111" alt="npm"/></a>
  <a href="https://www.nuget.org/packages/PDFluent"><img src="https://img.shields.io/nuget/v/PDFluent?label=NuGet&color=111111" alt="NuGet"/></a>
  <a href="https://central.sonatype.com/artifact/com.pdfluent/pdfluent"><img src="https://img.shields.io/maven-central/v/com.pdfluent/pdfluent?label=Maven&color=111111" alt="Maven Central"/></a>
  <br/>
  <a href="https://pdfluent.com/docs/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=badge_docs"><img src="https://img.shields.io/badge/docs-pdfluent.com-111111" alt="Documentation"/></a>
  <a href="https://github.com/pdfluent/pdfluent-sdk/discussions"><img src="https://img.shields.io/badge/discussions-ask%20a%20question-111111?logo=github" alt="GitHub Discussions"/></a>
  <a href="https://github.com/pdfluent/pdfluent-sdk/blob/main/LICENSE"><img src="https://img.shields.io/badge/SDK-AGPL--3.0%20%7C%20Commercial-111111" alt="SDK licence: AGPL-3.0 or commercial"/></a>
  <a href="https://pdfluent.com/download/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=badge_download"><img src="https://img.shields.io/badge/editor-free%20download-111111" alt="Editor: free download"/></a>
</p>

The engine is written in Rust with no C or C++ dependencies. The editor is free for everyone, including commercial use, and the SDK is AGPL-3.0 or commercially licensed.

---

## PDFluent Editor

The editor is free for everyone, including commercial use, with no account and no subscription. Documents are processed entirely on your device, and the only automatic network request is an update check you can switch off in Settings.

**[Download for macOS and Windows](https://pdfluent.com/download/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=editor_download)** · [Microsoft Store](https://apps.microsoft.com/detail/xpdbxj6xrlfqk2) · [Source](https://github.com/pdfluent/pdfluent) · [Licence](https://pdfluent.com/license/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=editor_license)

| Platform | Build |
|---|---|
| macOS | Universal binary (Apple Silicon and Intel), notarized |
| Windows | Installer, or the Microsoft Store |

---

## PDFluent SDK

The SDK is licensed under AGPL-3.0, or a commercial licence for anyone who cannot accept the AGPL's obligations. The commercial licence buys the right not to publish your source and unlocks no features; there is no licence key and every feature is in every build.

```bash
cargo add pdfluent                  # Rust
pip install pdfluent                # Python
npm install @pdfluent/node          # Node.js
npm install @pdfluent/sdk-wasm      # Browser (WebAssembly)
dotnet add package PDFluent         # .NET
```

Java is `com.pdfluent:pdfluent` on Maven Central; C and C++ link against the C API.

```rust
use pdfluent::prelude::*;

let doc = PdfDocument::open("in.pdf")?;
for page in doc.pages() {
    println!("{}", page.text()?);
}
```

```python
from pdfluent import Document

doc = Document("in.pdf")
for page in doc:
    print(page.extract_text())
```

```js
const { openPdf } = require('@pdfluent/node');

const doc = openPdf('in.pdf');
console.log(doc.extractText(0));
```

| Capability | Status |
|---|---|
| Text extraction with positions | Production |
| Rendering to PNG and JPEG (native bindings, not WebAssembly) | Production |
| AcroForm fill and flatten | Production |
| Digital signatures (PAdES B-B / B-T / B-LT) | Production |
| PDF/A validation and conversion (PDF/A-1b, 2b, 3b) | Production |
| Redaction that removes the content | Production |
| Merge, split, encryption | Production |
| XFA form flattening | Experimental |

→ [Documentation](https://pdfluent.com/docs/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=sdk_docs) · [Cookbook](https://pdfluent.com/cookbook/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=sdk_cookbook) · [Examples](https://github.com/pdfluent/examples) · [Source](https://github.com/pdfluent/pdfluent-sdk) · [Changelog](https://github.com/pdfluent/pdfluent-sdk/blob/main/CHANGELOG.md) · [Commercial licence](https://pdfluent.com/sdk/pricing/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=sdk_pricing) · [How we benchmark](https://pdfluent.com/benchmarks/how-we-measure/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=sdk_benchmarks)

---

## Community

Ask questions in [GitHub Discussions](https://github.com/pdfluent/pdfluent-sdk/discussions), in the Q&A category. Report bugs in the issue tracker of the repository the problem is in. Report security problems by email to [security@pdfluent.com](mailto:security@pdfluent.com), never in a public issue.

| You want to | Go to |
|---|---|
| Ask about the SDK | [SDK Discussions → Q&A](https://github.com/pdfluent/pdfluent-sdk/discussions/categories/q-a) |
| Ask about the editor | [Editor Discussions](https://github.com/pdfluent/pdfluent/discussions) |
| Show what you built | [Discussions → Show and tell](https://github.com/pdfluent/pdfluent-sdk/discussions/categories/show-and-tell) |
| Suggest a feature | [Discussions → Ideas](https://github.com/pdfluent/pdfluent-sdk/discussions/categories/ideas) |
| Report an SDK bug | [`pdfluent-sdk` issues](https://github.com/pdfluent/pdfluent-sdk/issues/new/choose) |
| Report an editor bug | [`pdfluent` issues](https://github.com/pdfluent/pdfluent/issues/new/choose) |
| Report a vulnerability | [security@pdfluent.com](mailto:security@pdfluent.com), see [SECURITY.md](https://github.com/pdfluent/.github/blob/main/SECURITY.md) |
| Buy a commercial licence | [sales@pdfluent.com](mailto:sales@pdfluent.com) |

---

## Repositories

| Repository | What is in it |
|---|---|
| [`pdfluent-sdk`](https://github.com/pdfluent/pdfluent-sdk) | The engine and every language binding. AGPL-3.0 or commercial. |
| [`pdfluent`](https://github.com/pdfluent/pdfluent) | The desktop editor: Tauri, React and TypeScript. Source-available. |
| [`examples`](https://github.com/pdfluent/examples) | Runnable SDK examples in Rust and the browser (WebAssembly). |
| [`hayro`](https://github.com/pdfluent/hayro) | Mirror of Laurenz Stampfl's pure-Rust PDF interpreter, which the rendering path builds on. |
| [`.github`](https://github.com/pdfluent/.github) | This page, and the default issue forms, contributing guide and security policy. |

---

<p align="center">Built by Innovation Trigger B.V. · <a href="https://pdfluent.com/?utm_source=github&utm_medium=referral&utm_campaign=org_profile&utm_content=footer">pdfluent.com</a></p>
