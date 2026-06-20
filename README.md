## Quey

**Verifiable randomness from a physical source.**

Quey extracts true randomness from photonic shot noise — a measurable physical process, not an algorithm. The entropy is hardware-sourced from a dedicated optical node, independently validated to NIST standards, and served via a REST API.

The randomness can be used two ways:

- **As raw entropy** — for Monte Carlo simulations, cryptographic seeding, procedural generation, generative art, A/B testing, or anywhere you need true physical randomness with auditable provenance.
- **As signed draws** — Ed25519-signed selections with public certificates, for giveaways, sortition, lotteries, or any selection where fairness must be provable to outside observers.

[**queyquantum.io**](https://queyquantum.io) · [Documentation](https://queyquantum.io/documentation) · [See a verified draw →](https://queyquantum.io/verify/89421ffc-6af3-427e-8123-fa6c799cc166)

---

### Repositories

- **[`quey-random-python`](https://github.com/QueyQuantum/quey-random-python)** — Official Python SDK. `pip install quey-random`. Eight methods covering raw bytes, random floats, NumPy arrays, sequence selection, and HKDF key derivation.
- **[`quey-verify-demo`](https://github.com/QueyQuantum/quey-verify-demo)** — Verify a Quey draw certificate locally in under 30 lines of Python or Node.js. Zero npm dependencies on the Node side.

### Independently validated

- **NIST SP 800-90B** — min-entropy 0.6236 bits/bit
- **NIST SP 800-22 (Rev 1a)** — 188 / 188 sub-tests passed (1 GB sample)
- **Shannon entropy** — 7.999994 bits/byte

### How signed draws work

For fairness-critical use cases, Quey produces Ed25519-signed certificates. Each certificate binds the draw's inputs, timestamp, and winning indices to a public key. Anyone can verify the signature offline using only public-key cryptography.

**Public key** (constant): `4fad999c2b586aab53155afc97f564a231350087b4c66d6a8f868963f42caf15`

---

Based in Israel · contact@queyquantum.io
