## Quey

**Verifiable randomness from a physical source.** Prove any selection is fair.

Quey extracts true randomness from photonic shot noise — a measurable physical process, not an algorithm. Every draw is signed with Ed25519 and published with a certificate that anyone can verify locally, in their browser, with zero trust in Quey.

[**queyquantum.io**](https://queyquantum.io) · [Documentation](https://queyquantum.io/documentation) · [See a verified draw →](https://queyquantum.io/verify/89421ffc-6af3-427e-8123-fa6c799cc166)

---

### Repositories

- **[`quey-random-python`](https://github.com/QueyQuantum/quey-random-python)** — Official Python SDK. `pip install quey-random`. Eight methods, four exceptions, NumPy-friendly.
- **[`quey-verify-demo`](https://github.com/QueyQuantum/quey-verify-demo)** — Verify a Quey draw certificate locally in under 30 lines of Python or Node.js. Zero npm dependencies on the Node side.

### Independently validated

- **NIST SP 800-90B** — min-entropy 0.6236 bits/bit
- **NIST SP 800-22 (Rev 1a)** — 188 / 188 sub-tests passed (1 GB sample)
- **Shannon entropy** — 7.999994 bits/byte

### How verification works

Each draw produces a certificate containing the draw ID, timestamp, input hash, participants, winning indices, and an Ed25519 signature over a canonical representation of those fields. Anyone with the public key can verify the signature offline — no API call, no server trust required.

**Public key** (constant): `4fad999c2b586aab53155afc97f564a231350087b4c66d6a8f868963f42caf15`

---

Based in Israel · contact@queyquantum.io
