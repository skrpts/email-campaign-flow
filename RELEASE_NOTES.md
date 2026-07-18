# Release Notes

## v1.2.0
GH#863 (K-045 intent/output mismatch) — the `email-campaign-writer` prompt, which produces the actual email campaign (the deliverable), was never invoked by the workflow: the pipeline built a brief, ran A/B analysis, and wrote subject lines but never wrote the emails. Wired it in as the last content step before language-polish via a new backing skill `email-campaign-composition` (`from_step` addressable), binding its inputs from upstream (campaign brief ← Audience Segmentation, subject lines ← Headline Writing) as explicit `context_params`. Re-pinned `polish-language`→1.0.6 and bound its `source` ← Email Campaign Composition so the output step polishes the campaign, not the positional previous step. Manifest skills 1→2, total 8→9.

## v1.1.26
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.25
GH#745 — declare per-step `output: {name, type}` on every execution step (campaign_brief/text, ab_test_analysis/text, subject_lines/list, polished_email/text). Lights up the #744 rich flow-map with named, typed outputs. Content-only; no bindings or logic changes.

## v1.1.24
GH#643 — declared GDPR + CAN-SPAM compliance. The skrpt generates marketing email copy and templates governed by these frameworks (mandates GDPR-compliant unsubscribe language, embeds the CAN-SPAM-required company address, unsubscribe and privacy links, and ships a GDPR marketing-compliance reference source). Declaring `requires.compliance: [gdpr, can-spam]` makes the manifest honest about what the workflow operates under; the scanner now resolves the previously-undeclared `compliance-gdpr` / `compliance-can-spam` findings to declared.

## v1.1.23
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 9 inline shared-content files and declare 9 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.22
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.21
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.20
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.19
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.18
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
