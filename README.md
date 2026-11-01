# Vault

**Prove a fact, not your whole identity.**

Vault is a self-sovereign identity wallet for Android. It stores your verifiable credentials on your phone and lets you share only the one fact a service needs, like "over 18", without handing over the document behind it. Every consent you give is logged on-chain, and you can revoke it at any time.

## Download

**[Download the APK](https://github.com/Priyasheoran006/Vault/releases/latest/download/vault.apk)** (about 28 MB)

If the link does not start a download, open the [Releases page](https://github.com/Priyasheoran006/Vault/releases) and tap `vault.apk` under Assets.

## Install

1. Open the download link on your Android phone and save the file.
2. Tap `vault.apk` to open it.
3. If Android asks, allow your browser or file manager to install apps from this source (Settings > Install unknown apps).
4. If Play Protect shows a warning, tap **Install anyway**. Vault is not on the Play Store, and Android shows this for any APK installed from outside it.
5. Open Vault from your app drawer.

## The problem

Proving one small fact online usually means uploading your full ID: name, address, ID number and photo. Every bank, clinic and website asks for a fresh copy, and those copies pile up on servers you cannot see into or take data back from. When one of those databases is breached, everyone in it is exposed.

## What Vault does

- **Holds your credentials.** Verifiable credentials from trusted issuers live in your wallet, not on someone else's server.
- **Shares only what is needed.** Prove your age, KYC status or eligibility without revealing the underlying document.
- **Revokes instantly.** See every access grant in one dashboard and cancel any of them.
- **Keeps a tamper-proof record.** Each consent grant and revocation is written to a public ledger that no single party controls.
- **Enforces revocation.** Smart contracts make a revoked grant stop working, instead of just marking it expired.

## How it works

1. **Issue.** A trusted authority issues a verifiable credential to your wallet.
2. **Disclose.** A verifier asks a question and you share only the proof that answers it.
3. **Verify.** The verifier checks the proof without ever seeing your raw data.
4. **Revoke.** You cancel access at any time and the contract enforces it.

## Tech stack

- Flutter and Dart for the mobile wallet
- W3C Decentralized Identifiers (DID) and Verifiable Credentials
- Zero-knowledge proofs for attribute checks without revealing data
- Solidity smart contracts for consent and revocation logging, run on Hardhat and Polygon testnets

## Where it is useful

- **Individuals** get control over sensitive data and decide when sharing stops.
- **Institutions** avoid storing full document copies they never needed, which lowers compliance load and liability.
- **Migrant workers and others without stable paperwork** get a portable, verifiable identity that travels with them.
- **Banking KYC, healthcare and education** can all use the same selective disclosure flow.

## Status

Vault is a working prototype. The wallet interface, consent logging on a local testnet and the selective disclosure demo are built. Next steps are a pilot with a real issuer on a public testnet, then a mainnet move with more issuer types.

## Note

This repository only hosts the release build of the app. The source code is private.
