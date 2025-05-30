---
id: work-proof
title: Work Proof
hide_table_of_contents: false
---
import useBaseUrl from '@docusaurus/useBaseUrl';

# Work Proof

ARO introduces a novel protocol to provide trusted workload proofs for heterogeneous edge nodes, named **GPoW**(**Guarantee Proof of Work**).

### Overview

The **GPoW** (**Guarantee Proof of Work**) protocol is a core feature of the ARO network, designed to provide trusted resource and workload proofs for heterogeneous edge nodes, including network bandwidth, storage, computing power, etc.&#x20;

Unlike traditional systems which focuses only on one type of resource like storage verification, GPoW extends its capabilities to support various types of workloads such as CDN traffic and GPU computing tasks, making it a versatile proof mechanism for DePIN networks.

### Resource Virtualization and Integration

In the first phase, ARO utilizes virtualization and containerization technologies to standardize the integration of diverse hardware resources. This allows the network to incorporate a wide range of devices, including enterprise servers, personal PCs, mobile devices, and even WASM environments within browser plugins. Using technologies like Docker and Kubernetes, these resources are virtualized to create a standardized execution environment, enabling them to perform various tasks efficiently.

### Work Proof Generation

The core of GPoW is to generate trusted and verifiable workload proofs for different resource types. It combines several advanced mechanisms:

* **Trusted Execution Environment (TEE):** Using TEE, GPoW ensures that the resource usage proof is securely generated without tampering. TEE isolates the execution environment, generating encrypted and signed workload proofs that can be securely verified. This approach guarantees the authenticity of the reported workload for tasks like data storage, network transmission, or computational processing.
* **Zero-Knowledge Proofs (ZK):** GPoW incorporates zkVM (Zero-Knowledge Virtual Machine) to verify complex computations, such as GPU tasks, without revealing underlying data. This allows the network to validate workload contributions without exposing sensitive details, ensuring privacy and security.
* **Random Challenge Mechanism:** To prevent nodes from faking workload contributions, GPoW will also use random challenge approach. The network issues random requests to nodes, which must respond promptly with valid workload proofs. This strategy mitigates risks from sybil attacks and fraud reporting.

### On-Chain Verification and Settlement

Once the workload proof is generated, it is submitted to the blockchain's GPoS module for validation. This process includes:

* **Proof Verification:** On-chain logic verifies the submitted proofs using TEE attestations and zk-generated proofs.
* **Incentives and Penalties:** Verified nodes receive token rewards, while nodes submitting fraud or delayed proofs face penalties. This mechanism ensures fair participation and discourages dishonest behavior.
* **Transparent Settlement:** All transactions and proof verifications are recorded on-chain, providing transparency and allowing participants to monitor their contributions and rewards.

### Security and Scalability

To safeguard against potential security threats like sybil attacks or proof forgery, GPoW integrates multiple layers of verification using TEE and zero-knowledge proofs. This ensures the reliability of the proofs generated by the nodes. Additionally, GPoW is designed to be modular and extensible, allowing the network to support new resource types and adapt to varying application scenarios.

### Conclusion

GPoW (Guarantee Proof of Work) is an innovative proof mechanism designed in the ARO network that leverages TEE, zkVM, and random challenge techniques to validate the workloads of heterogeneous resource nodes.&#x20;

By providing end-to-end solutions from resource virtualization to on-chain verification, GPoW ensures the integrity, transparency, and security of the ARO network, enabling efficient and trustworthy decentralized service delivery.