# pqcrypto

Maintained fork of [pqcrypto](https://github.com/rustpq/pqcrypto) — Rust bindings to post-quantum cryptographic algorithms from [PQClean](https://github.com/PQClean/PQClean).

This fork uses [Bubbler's PQClean fork](https://github.com/Bubbler-Messaging/PQClean) as the native backend, with a frozen version of the C implementations.

## What changed from upstream

- **Actively maintained** for [Bubbler Messaging](https://github.com/Bubbler-Messaging)
- Rust edition 2024
- PQClean submodule points to Bubbler's fork (version frozen)

## Included algorithms

| Crate | Type | Algorithms |
| :---- | :--- | :--------- |
| `pqcrypto-mlkem` | KEM | ML-KEM-512, ML-KEM-768, ML-KEM-1024 |
| `pqcrypto-mldsa` | Signature | ML-DSA-44, ML-DSA-65, ML-DSA-87 |
| `pqcrypto-falcon` | Signature | Falcon-512, Falcon-1024, Falcon-padded variants |
| `pqcrypto-sphincsplus` | Signature | SPHINCS+-SHA2/SHAKE (128/192/256, f/s) |
| `pqcrypto-classicmceliece` | KEM | Classic McEliece variants |
| `pqcrypto-hqc` | KEM | HQC-128, HQC-192, HQC-256 |

## Building

A C compiler (`cc`, `clang`, ...) is required to build the PQClean C implementations.

```bash
git clone https://github.com/Bubbler-Messaging/pqcrypto.git
cd pqcrypto
git submodule update --init --recursive
cargo build
```

## Testing

```bash
cargo test
```

## License

Licensed under either of

- [Apache License, Version 2.0](pqcrypto/LICENSE-APACHE)
- [MIT License](pqcrypto/LICENSE-MIT)

at your option.
