# Contributing to PDFluent

Thanks for your interest in PDFluent.

This is the default guide for PDFluent repositories. A repository that ships its
own `CONTRIBUTING.md` overrides this one — read that one instead.

## Reporting bugs

Open an issue in the repository the problem is in:

- [pdfluent/pdfluent](https://github.com/pdfluent/pdfluent) — the desktop editor
- [pdfluent/pdfluent-sdk](https://github.com/pdfluent/pdfluent-sdk) — the SDK and its documentation
- [pdfluent/examples](https://github.com/pdfluent/examples) — the runnable examples

Include steps to reproduce, what you expected, what happened instead, your
operating system, and the PDFluent version. A PDF that triggers the problem is
worth more than any description — attach one only if you are free to share it.

## Reporting a security problem

Do not open a public issue. Follow
[SECURITY.md](https://github.com/pdfluent/.github/blob/main/SECURITY.md).

## Contributing code

**Ask before you write.** PDFluent does not accept code under a blanket inbound
licence, and this guide grants none. The licensing of the SDK and of the editor
differs, and the SDK's is in the middle of a change; accepting code on standing
terms now would fix terms that are not settled yet.

So: open an issue describing the change you have in mind, or write to
license@pdfluent.com, and we will sort out the arrangement before you start. If
a pull request lands without that conversation, it may have to be closed
unmerged — which costs you the work, not us. That is the only reason this
section is at the top of the process instead of the bottom.

## Once an arrangement is in place

- Rust: follow `cargo clippy`
- TypeScript: the ESLint config in the repository you are working in
- Commits: conventional commits (`feat:`, `fix:`, `docs:`, …)
- Keep a pull request to one change
- Add tests where the change can be tested, and update the documentation if you
  change behaviour anyone can see
- File headers: copy the header the surrounding files already carry. It differs
  per repository, and it is not yours to pick.

Build instructions live in each repository's `README`.

## Licence

Every PDFluent repository states its own terms in its `LICENSE` or `LICENSE.md`.
Nothing in this file grants a licence, and nothing in it takes one.
