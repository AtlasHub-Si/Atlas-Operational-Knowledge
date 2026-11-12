# Operational Knowledge publishing standard v0.1

## Required frontmatter

`document_id`, `tenant_id`, `business_unit_id`, `department_id`, `type`, `classification`, `version`, `status`, `owner_role`, `approved_by`, `effective_at`, `review_due_at`, `language`, `allowed_roles`.

Field presence is not permission: server-side policy is authoritative. Any change to an approved document that changes customer-facing content requires a new version and review.

## Lifecycle

- `draft`: editor is working on an unpublished document.
- `review_requested`: designated reviewer checks correctness, legal/brand compliance and source.
- `approved`: human or explicitly authorized workflow records approval against content hash and version.
- `published`: document becomes queryable by permitted agent roles.
- `deprecated`: outdated but retained for audit; not retrievable for current use.
- `revoked`: immediately block retrieval, invalidate caches and index entries.

Do not allow an LLM/agent to self-approve its own product-facing instructions. Record provenance and refusal reasons. Use stable IDs and versioned citations.

## Source-of-truth

- CRM owns lead/customer records; order systems own orders; pricing service owns current price.
- Knowledge docs own approved **instructions for how to respond**, not up-to-the-minute operational data.
- Real personal data, secrets or HR cases must never be committed here.

## Pilot acceptance

1. Approved document retrieved by correct role.
2. Draft/revoked/unapproved document denied.
3. BU01 does not retrieve BU03-DEMO content.
4. The reply cites exact document ID and version.
5. Every action is logged with request ID and policy decision.
