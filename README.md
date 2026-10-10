# Sponsor Cap Auditor

<!-- three.ws:badges -->
[![GitHub stars](https://img.shields.io/github/stars/nirholas/sponsor-cap-auditor?style=flat&logo=github)](https://github.com/nirholas/sponsor-cap-auditor/stargazers) [![Last commit](https://img.shields.io/github/last-commit/nirholas/sponsor-cap-auditor?style=flat)](https://github.com/nirholas/sponsor-cap-auditor/commits) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat)](https://github.com/nirholas/sponsor-cap-auditor/pulls) [![AI agent friendly](https://img.shields.io/badge/AI%20agents-AGENTS.md%20%2B%20llms.txt-6d5dfc?style=flat)](https://github.com/nirholas/sponsor-cap-auditor/blob/HEAD/AGENTS.md)
<!-- /three.ws:badges -->


Model fee and resource caps from v1 transactionConfig for paymasters and co-signers.

## Why this exists

Solana transaction v1 raises the maximum transaction size from 1,232 to 4,096 bytes. Sponsor Cap Auditor explores a focused consumer use of that space while making the wire budget visible.

## Working features

- Responsive monochrome product UI with deterministic payload generation
- Live UTF-8 byte meter, v1 fit estimate, and legacy transaction comparison
- Wallet Standard discovery and v1 capability reporting
- Copy and download flows with no server, account, analytics, or custody
- Dependency-free production build and Cloudflare Workers static configuration
- Product contract test, security headers, security policy, and architecture docs

## Status

This is a functional product prototype, not an audited transaction broadcaster. It intentionally stops at payload generation so users cannot mistake experimental sizing logic for a reviewed signing flow. Integrate the generated artifact with [First](https://github.com/nirholas/first-onchain) or a reviewed `@solana/kit >= 8` v1 sender.

## Run

```bash
npm test
npm run build
npm run dev
```

Open http://localhost:4173. To deploy after authenticating Wrangler, run `npm run deploy`.

## Transaction v1 rules

- Use transaction version 1 to access the 4,096-byte ceiling.
- Set compute-unit and loaded-accounts-data-size limits explicitly; v1 defaults both to zero.
- Check `supportedTransactionVersions.has(1)` before asking a wallet to sign.
- Readers must set `maxSupportedTransactionVersion: 1`.
- Read sponsor and indexer limits from `transactionConfig`, not Compute Budget instructions.
- V1 supports 64 inline addresses, rejects duplicates, and does not use address lookup tables.

See [docs/PRODUCT.md](docs/PRODUCT.md) for product boundaries and extension points.

## License

MIT

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=nirholas/sponsor-cap-auditor&type=Date)](https://www.star-history.com/#nirholas/sponsor-cap-auditor&Date)

<!-- three.ws:growth -->
## Support the project

If sponsor-cap-auditor saves you time, **[star it on GitHub](https://github.com/nirholas/sponsor-cap-auditor)**. Stars are how other developers and AI agents find the repositories worth trusting, and they cost you one click.

Know someone who would use it? [Post on X](https://twitter.com/intent/tweet?text=sponsor-cap-auditor%3A%20Model%20fee%20and%20resource%20caps%20from%20v1%20transactionConfig%20for%20paymasters%20and%20co-signers&url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fsponsor-cap-auditor) · [Share on Bluesky](https://bsky.app/intent/compose?text=sponsor-cap-auditor%3A%20Model%20fee%20and%20resource%20caps%20from%20v1%20transactionConfig%20for%20paymasters%20and%20co-signers%20https%3A%2F%2Fgithub.com%2Fnirholas%2Fsponsor-cap-auditor) · [Share on LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fsponsor-cap-auditor) · [Submit to Hacker News](https://news.ycombinator.com/submitlink?u=https%3A%2F%2Fgithub.com%2Fnirholas%2Fsponsor-cap-auditor&t=sponsor-cap-auditor%3A%20Model%20fee%20and%20resource%20caps%20from%20v1%20transactionConfig%20for%20paymasters%20and%20co-signers) · [Share on Reddit](https://www.reddit.com/submit?url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fsponsor-cap-auditor&title=sponsor-cap-auditor%3A%20Model%20fee%20and%20resource%20caps%20from%20v1%20transactionConfig%20for%20paymasters%20and%20co-signers)

## Built for AI agents too

Coding agents and LLM tooling can read this repo directly: [AGENTS.md](./AGENTS.md), [llms.txt](./llms.txt), [llms-full.txt](./llms-full.txt). Point an agent at `https://github.com/nirholas/sponsor-cap-auditor` and it has the context it needs.

## More from the same author

- [All repositories by nirholas](https://github.com/nirholas/nirholas#readme): the full catalog, grouped by topic
- [three.ws](https://three.ws): the platform for 3D AI agents with Solana wallets, a skill marketplace and x402 payments
- Questions or ideas: [open an issue](https://github.com/nirholas/sponsor-cap-auditor/issues) or [start a discussion](https://github.com/nirholas/sponsor-cap-auditor/discussions)

## Contributors

[![Contributors](https://contrib.rocks/image?repo=nirholas/sponsor-cap-auditor)](https://github.com/nirholas/sponsor-cap-auditor/graphs/contributors)

<!-- /three.ws:growth -->
