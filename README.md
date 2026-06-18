I build tools for self-hosters and homelab operators, mostly around Docker, Portainer, DNS, and network privacy.

### Projects

- **[hosaka](https://github.com/nopoz/hosaka)** [![release](https://img.shields.io/github/v/release/nopoz/hosaka)](https://github.com/nopoz/hosaka/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/hosaka/ci.yml?label=CI)](https://github.com/nopoz/hosaka/actions/workflows/ci.yml) 
  Docker image update monitor with semver-aware classification, one-click upgrades, live console output, and notifications via Slack, Discord, Telegram, and more.

- **[pfsense-dnscrypt-proxy](https://github.com/nopoz/pfsense-dnscrypt-proxy)** [![release](https://img.shields.io/github/v/release/nopoz/pfsense-dnscrypt-proxy)](https://github.com/nopoz/pfsense-dnscrypt-proxy/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/pfsense-dnscrypt-proxy/ci.yml?label=CI)](https://github.com/nopoz/pfsense-dnscrypt-proxy/actions/workflows/ci.yml)
  A pfSense package bringing DNSCrypt, DoH, Oblivious DoH, and Anonymized DNS to your firewall with a full GUI. Signature-verified builds with SLSA provenance.

- **[portrieve](https://github.com/nopoz/portrieve)** [![release](https://img.shields.io/github/v/release/nopoz/portrieve)](https://github.com/nopoz/portrieve/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/portrieve/ci.yml?label=CI)](https://github.com/nopoz/portrieve/actions/workflows/ci.yml)
  Back up, restore, and migrate Portainer stacks as plain, git-friendly Docker Compose files. Fills the gap between blunt database backups and manual exports.

### Security & CI/CD

I treat the pipeline as part of the product. Practices I apply across my projects and contributions:

- Default-deny GitHub Actions permissions (`permissions: {}`), with each job opting back into the least scope it needs.
- Third-party actions pinned to commit SHAs rather than mutable tags, to close supply-chain gaps.
- Layered scanning: secret detection (gitleaks), workflow auditing (actionlint, zizmor), dependency review, Dockerfile and image scanning (hadolint, Trivy), and CodeQL static analysis.
- Signed, attested release artifacts (SLSA provenance) so downstream users can verify what they install.

### Also contribute to

[Home Assistant](https://github.com/home-assistant/core) · [odysseus](https://github.com/pewdiepie-archdaemon/odysseus)

### Focus areas

Self-hosting · Encrypted DNS · Docker tooling · pfSense / FreeBSD packaging · CI/CD supply-chain security
