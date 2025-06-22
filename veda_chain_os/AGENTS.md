# AGENTS.md - VEDA Chain OS Development Guidelines

This document provides high-level guidelines for agents contributing to the VEDA Chain OS project.

## 1. General Principles
    - **Decentralization First**: All design and implementation choices should prioritize decentralization.
    - **Security by Design**: Implement robust security measures at all layers, with a focus on quantum security where applicable.
    - **Modularity**: Design components to be as modular and independent as possible to facilitate parallel development and maintenance.
    - **Clarity and Readability**: Code should be well-documented and easy to understand.

## 2. Language Choices
    - **Smart Contracts**: Rust will be the primary language for smart contract development due to its performance and safety features.
    - **Blockchain Core**: Core blockchain components (e.g., consensus, networking) will primarily use Rust. Other languages like Go or C++ might be considered for specific modules if there's a strong justification.
    - **AI Components**: Python is preferred for AI/ML development, leveraging its rich ecosystem of libraries.
    - **OS Development**: C and Rust are to be used for kernel-level and OS development.
    - **Tooling & dApps**: Flexible, but prioritize languages that integrate well with the core VEDA ecosystem (e.g., Rust, JavaScript/TypeScript for frontends).

## 3. Coding Conventions
    - **Style Guides**: Follow standard style guides for each language (e.g., Rustfmt for Rust, PEP 8 for Python).
    - **Comments**: Write clear and concise comments. Explain the "why" not just the "what". Document public APIs thoroughly.
    - **Testing**:
        - Strive for high test coverage.
        - Include unit tests, integration tests, and end-to-end tests where appropriate.
        - Test-Driven Development (TDD) is encouraged.
    - **Error Handling**: Implement robust error handling. Avoid silent failures.
    - **Commit Messages**: Follow conventional commit message formats (e.g., `feat: add new consensus mechanism`).

## 4. Version Control
    - **Branching Strategy**: Use a Gitflow-like branching model (main, develop, feature branches).
    - **Pull Requests**: All code changes must be submitted via pull requests and require at least one review (even from an AI agent peer, if applicable in the future).

## 5. Documentation
    - Maintain up-to-date documentation for all modules and APIs.
    - Use Markdown for documentation files.

## 6. Specific Layer Guidelines

### 6.1. Base Layer – Quantum-Secure Blockchain
    - Cryptographic Primitives: Use NIST-approved or well-vetted post-quantum cryptographic algorithms. Lattice-based cryptography is the current focus.
    - Consensus: Clearly define the interaction between PoS and AI validators.
    - Smart Contract DSL: The AI-optimized DSL for Rust smart contracts should be designed for security, efficiency, and ease of use.

### 6.2. AI Layer
    - Model Training: Prioritize federated learning for privacy.
    - Agent Design: Autonomous AI agents should be designed with clear roles, permissions, and resource limits.

### 6.3. OS Layer
    - Security: Kernel-level process separation and secure containers are paramount.
    - Decentralized Storage: Integrate IPFS and DAG-based file systems seamlessly.

## 7. Future Iterations
    - These guidelines will evolve as the project progresses. Check this file regularly for updates.
    - Specific sub-directories may contain their own `AGENTS.md` files with more focused guidelines. These will take precedence for the files within their scope.

This `AGENTS.md` is a living document. Contributions and suggestions for improvement are welcome.
