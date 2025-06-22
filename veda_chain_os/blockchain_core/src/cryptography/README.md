# Cryptography Module

This module is responsible for all cryptographic operations within the VEDA Chain OS blockchain core.
Its primary focus is to implement and manage post-quantum cryptographic algorithms to ensure long-term security against quantum threats.

## Submodules

-   **`lattice_based/`**: Contains implementations and wrappers for lattice-based cryptography. This is the current focus for post-quantum security, aligning with recommendations from cryptographic bodies like NIST.
    -   We will be using specific crates from the `pqcrypto` suite (e.g., `pqcrypto-kyber`, `pqcrypto-dilithium`) provided by the RustCrypto organization. These crates offer bindings to well-vetted implementations of lattice-based post-quantum cryptographic algorithms, such as Kyber for Key Encapsulation Mechanisms (KEMs) and Dilithium for digital signatures, which are finalists/winners in the NIST PQC standardization process.

## Design Principles
-   **Security First**: Utilize well-vetted algorithms and libraries.
-   **Modularity**: Cryptographic functions should be exposed through a clear and consistent API, making it easier to update or replace algorithms in the future.
-   **Performance**: While security is paramount, performance considerations for on-chain operations will be taken into account.

This module will evolve as the project progresses and as the landscape of post-quantum cryptography matures.
