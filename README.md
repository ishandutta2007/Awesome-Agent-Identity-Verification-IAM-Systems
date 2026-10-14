# Awesome-Agent-Identity-Verification-IAM-Systems

# Top Agent Identity Verification & IAM Systems Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Non-Human Identity Management, Agent Credentialing & Delegated Authorization*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Agent Identity Verification & IAM**. These tools enable organizations to treat AI agents as first-class non-human identities with their own lifecycle, least-privilege scopes, cryptographic credentials, and audit trails—answering "who is this agent?" and "what is it authorized to access?" .

**Examples** include Descope, WorkOS, Clerk, Auth0, Stytch, Frontegg, Okta, Ping Identity, CyberArk, and Beyond Identity (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, verifiable agent credentials, and open IAM stacks—ideal for platform engineers, security architects, and developers seeking transparent, vendor-independent agent identity infrastructure.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Okta](https://www.okta.com/)**  
  Enterprise IAM with agent identity features. Named a Leader in the 2026 ISG Buyers Guide for Non-Human Identities Platforms, with agent identity capabilities added in Q1-Q2 2026 . Offers Cross App Access for delegated agent authorization .

- **[CyberArk](https://www.cyberark.com/)**  
  Leader in Non-Human Identity Management per ISG 2026, with exemplary ratings across Product Experience categories . Conjur provides secrets management for machine identities. Acquired Venafi in 2024 for certificate-based machine identity .

- **[Descope](https://www.descope.com/)**  
  Agent identity platform with per-agent identities, tool-level scopes, and audit. Version 2.0 (January 2026) added agents as first-class identities with agent directory. Supports OAuth 2.1, DCR, token exchange, ID-JAG, and Cross-App Access. Free tier: 7,500 MAU, 2,000 consents, 2,000 tokens .

- **[WorkOS](https://workos.com/)**  
  AuthKit described as a spec-compatible authorization server for MCP, with dynamic client registration, OAuth-protected resource metadata, and PKCE. Standalone Connect allows keeping existing login UI while delegating MCP client authorization .

- **[Stytch](https://stytch.com/)**  
  Connected Apps turns your app into an identity provider so agents act on users' behalf. Implements OAuth 2.1, dynamic client registration, RBAC scopes, and device authorization for human approval. Core rule: "Users can only give an app the same permissions they themselves have." Free tier: 10,000 MAU + agents .

- **[Auth0](https://auth0.com/)**  
  Supports OAuth 2.1, DCR, PKCE, and JWKS for MCP authorization. Teams write Actions to map MCP client registrations to the right tenant. Auth0's MCP server is for managing the tenant, not for protecting MCP servers .

- **[Clerk](https://clerk.com/)**  
  OAuth 2.1 support with JWKS at discoverable endpoints. DCR supported on certain plan tiers. Dedicated MCP documentation was thinner as of mid-2026 but expanding .

- **[Frontegg](https://frontegg.com/)**  
  Customer identity platform with agent identity capabilities for B2B SaaS applications.

- **[Ping Identity](https://www.pingidentity.com/)**  
  Rated "Innovative" in the 2026 ISG IAM Buyers Guide for Product Experience . Offers agentic IAM products launched Q1-Q2 2026 .

- **[Beyond Identity](https://www.beyondidentity.com/)**  
  Passwordless authentication with device-bound credentials. Rated "Merit" in the 2026 ISG IAM Buyers Guide .

## Open-Source GitHub Projects

- **[ThunderID (WSO2)](https://github.com/Malith-19/thunder)**  
  Lightweight, Go-based IAM stack built to secure humans, AI agents, and machines (Apache-2.0). Designed for the agentic era with **agent-native identity**—managing AI agents as first-class identities with delegated authority, consent-aware access, and traceability. Features **post-quantum-safe by design** with crypto-agile foundation, **decentralized identity** support (DIDs, verifiable credentials, OpenID4VCI/OpenID4VP), OAuth 2.1 with PAR and PKCE, and **declarative GitOps-ready** YAML resource definitions. Includes MCP server for managing IAM from AI agents .

- **[SoulAuth (TrantorLabs)](https://github.com/TrantorLabs/SoulAuth)**  
  Rust-based identity infrastructure with explicit security boundaries (license varies). Features **AI actor identity** via Ed25519 challenge-response—no email, no password, no user row. Supports multiple active keys per identity, so each machine holds its own and the log records which key authenticated. Includes OIDC provider with PKCE, MFA (TOTP), server-side sessions, and **tamper-evident audit**. ~24k lines of Rust, 196 unit tests, 77 architecture invariants .

- **[AGNTCY Identity (Linux Foundation)](https://github.com/agntcy/identity-service)**  
  Open-source agent identity infrastructure (Apache-2.0) from the AGNTCY project—a Linux Foundation initiative with 75+ collaborating organizations. Defines identity assignment with **open** (no centralized authority), **collision-free** (UUID per entity), and **verifiable** (Verifiable Credential as Identity Badge) properties. Supports W3C DIDs and VCs. Features **Task/Tool-Based Access Control (TBAC)** with optional human-in-the-loop approval. Demo includes Financial Assistant with agents and MCP server .

- **[OpenA2A AIP](https://datatracker.ietf.org/doc/html/draft-fane-opena2a-aip-02)**  
  IETF Internet-Draft for Agent Identity Protocol (AIP). Defines three conformance levels: **Local Identity** (SDK/CLI, Ed25519 keypair), **Managed Identity** (identity provider with trust scoring and centralized audit), and **Federated Identity** (DID resolution, verifiable credentials, cross-platform trust). Uses Ed25519 with hybrid ML-DSA-65 for post-quantum readiness. Agent identifier format: `aim_` + first 8 hex chars of SHA-256 public key digest .

- **[SPIFFE/SPIRE](https://github.com/spiffe/spire)**  
  Open standard for workload identity (Apache-2.0). Issues short-lived, verifiable identities to workloads and agents without long-lived secrets. Widely adopted as the foundation for zero-trust machine identity. Listed in the 2026 NHI management tools guide as the open standard for workload identity .

- **[Keycloak](https://github.com/keycloak/keycloak)**  
  Leading open-source IAM (Apache-2.0). Features SSO, social login, MFA, LDAP/AD integration, SAML, OIDC, and comprehensive admin console. Foundation for many enterprise identity deployments. Rated "Merit" in the 2026 ISG IAM Buyers Guide .

- **[Ory](https://github.com/ory)**  
  Modular, cloud-native identity stack (Apache-2.0). Components include Ory Kratos (identity management), Ory Hydra (OAuth2/OIDC), and Ory Keto (authorization). API-first design optimized for Kubernetes. AGNTCY demo supports Ory as an IdP for agent onboarding .

- **[ZITADEL](https://github.com/zitadel/zitadel)**  
  Open-source identity infrastructure (Apache-2.0) built for multi-tenancy. Features SSO, MFA, Passkeys, OIDC, SAML, SCIM, LDAP, and comprehensive audit trail via immutable event stream .

- **[Authentik](https://github.com/goauthentik/authentik)**  
  Open-source Identity Provider (MIT) for modern SSO. Supports SAML, OAuth2/OIDC, LDAP, RADIUS. Designed for self-hosting from small labs to large production clusters .

- **[Teleport](https://github.com/gravitational/teleport)**  
  Infrastructure identity platform (AGPL-3.0) named an Overall Leader in KuppingerCole's 2026 Zero Trust Platforms report. Certificate-backed, secretless approach securing humans, machines, workloads, and AI agents. Provides Zero Trust access to MCP servers that agents depend on. Short-lived certificate model with mature access workflows .

- **[Aembit](https://aembit.io/)**  
  Workload and agent identity platform (open-core) for secretless, policy-based access between workloads. Brokers just-in-time access without stored credentials. Positioned for the shift from long-lived secrets to short-lived identity .

- **[AgentID](https://github.com/AgentID)**  
  Open-source agent identity provider for the case where agents arrive at your app as prospective customers from organizations you have no relationship with. Add AgentID as a custom OIDC provider in Clerk, Supabase, Auth0, Better Auth, or Auth.js .

### Additional Strong Open-Source Options

- **[FusionAuth](https://github.com/FusionAuth/fusionauth)** — Developer-focused identity platform (Apache-2.0 for community) with SSO, MFA, and extensive API/SDK support .
- **[Logto](https://github.com/logto-io/logto)** — Open-source IAM (MPL-2.0) for modern apps with OIDC, SAML, MFA, RBAC, and organization-scoped login .
- **[Hanko](https://github.com/teamhanko/hanko)** — Open-source authentication (AGPL-3.0) with passkeys, social logins, SAML SSO, and MFA .
- **[SimpleSAMLphp](https://github.com/simplesamlphp/simplesamlphp)** — Native PHP authentication application (LGPL-2.1) for SAML federation .
- **[pac4j](https://github.com/pac4j/pac4j)** — Security engine for Java (Apache-2.0) supporting OAuth, CAS, SAML, OIDC, LDAP, JWT .
- Community **n8n** workflows for agent identity provisioning and audit alerting.

**Frameworks for building custom systems**: Combine **ThunderID** or **SoulAuth** as the core IAM stack with **SPIFFE/SPIRE** for workload identity, **AGNTCY Identity** for verifiable agent credentials, **Teleport** for MCP server access governance, and **PostgreSQL/SurrealDB** for persistence—creating a fully self-hosted, enterprise-grade agent identity verification platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Agent identity systems handling authentication and authorization must comply with security standards (SOC 2, ISO 27001, GDPR, etc.).
- Self-hosted open-source solutions require proper security hardening, cryptographic key management, and ongoing maintenance. Agentic IAM is an emerging field—only 18% of professionals say they are highly confident their IAM can handle agents (Cloud Security Alliance / Strata, February 2026) . Standards frameworks from IETF, NIST, and W3C are still maturing .

---

**Made for security architects, platform engineers, IAM administrators, and developers building transparent agent identity solutions.**  
Let's make Agent Identity Verification & IAM more open, data-driven, and trustworthy.
