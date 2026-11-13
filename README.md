# Atlas-Operational-Knowledge

**Operational knowledge for the Atlas-Harness ecosystem — controlled, versioned and agent-readable.**

**Status:** Architecture / fictional pilot only. This is an original Atlas repository; **not** a fork of the Obsidian application. The underlying Markdown content can be edited with Obsidian or any compatible editor; runtime access occurs via authenticated Atlas services.

## Scope

- Approved operational knowledge for business units: product playbooks, scripts, FAQs, disclaimers and customer-service procedures.
- Editorial lifecycle: draft, review requested, approved, published, deprecated or revoked.
- Machine-readable metadata and provenance: tenant, BU, owner, role permissions, version, approval, effective date, review due date and source.
- Integration with Atlas-Memory-Fabric behind access controls.

**Not in scope:** raw customer/HR records, real prices, CRM balances, transactional state, company secrets, live credentials and unreviewed prompts.

## Start here

- [Publishing policy](docs/publishing-policy.md)
- [Synthetic BU03 demo product](examples/BU03-DEMO/products/demo-product/README.md)
- [Atlas-Harness memory domain design](https://github.com/AtlasHub-Si/Atlas-Harness/blob/main/docs/memory-knowledge.md)
- [Atlas-Harness architecture ADR](https://github.com/AtlasHub-Si/Atlas-Harness/blob/main/docs/adr/0001-atlas-harness-architecture.md)

## Knowledge life cycle

Draft -> review_requested -> approved -> published -> deprecated/revoked. Only published, current documents may be retrieved by appropriate roles. Index entries must be invalidated on revocation.

Obsidian is an **optional authoring interface**. We do not ship Obsidian's proprietary editor or imply it is open-source. An Atlas-developed plugin may be evaluated later using the official sample-plugin template and its own license.

## Initial milestone

A restricted Atlas-Agent can retrieve and cite one approved fictional product FAQ through Atlas-Memory-Fabric. The runtime receives the allowed document version but cannot edit it, view other BU knowledge, or initiate real customer communications.


## Ownership and support

This repository contains original Atlas project materials and synthetic examples. The limited rights-reservation notice in [LICENSE](LICENSE) applies only to actually Atlas-owned original contributions. Company references: [LEGAL.md](LEGAL.md). **Legal:** legal@Atlas-SI.com · **Support:** support@AtlasHub.SI. **Curator:** [SergioMonteiro-Atlas](https://github.com/sergiomonteiro-atlas).
