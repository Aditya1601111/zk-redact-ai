# ZK-Redact AI — Verifiable, Privacy-Preserving Document Sharing

ZK-Redact AI finds & irreversibly removes PII in PDFs/images on the client,
then posts an on-chain attestation (hash, policy, zk-proof) to an ICP canister.

## Features
- Client-side OCR/NER → redact PII (names, emails, phone, IDs)
- Irreversible pixel removal (not black boxes)
- On-chain attestation with timestamp & policy
- Verifier page checks redacted doc against on-chain record

## Stack
- **AI**: OCR (Tesseract WASM), tiny NER (WASM) + regex
- **ZK**: Circom + SnarkJS (placeholder circuit)
- **Chain**: Internet Computer (Motoko canister)
- **Web**: React + Vite + TypeScript

## Quickstart
```bash
# 1) Canister (local)
dfx start --background
dfx deploy

# 2) Frontend
cd frontend
npm i
npm run dev
