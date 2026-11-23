# Sim Record

A public, append-only record of a simulated run, starting at row one. Every row in this
repository describes what a deterministic check did to a synthetic input. Nothing here is a
conversation, and nothing here describes a person.

**Prototype. Research and educational use only.** Not for production, commercial deployment, or
safety-critical environments. All systems described here are experimental and may contain defects.

**Licence: CC BY-NC-ND 4.0.** Share it, quote it, check it. Do not sell it, and do not publish a
modified version under this licence.

---

## Read the limits before the numbers

This section is first because the numbers are meaningless without it. Each line below is a claim
someone might reasonably make about a record like this, and what is actually true of this one.

| Claim | What is true |
|---|---|
| "PASS means the answer was correct." | **PASS means no rule fired.** A row can pass because it was checked and verified, or because there was nothing to check. Those are different outcomes and the row records which one it was. |
| "The gate verified most of what it passed." | At the 121 PASS verdicts measured on 2026-11-22, **116 (95.9%) verified nothing**, because no claims were declared to check. Verification cannot exceed declaration. |
| "The gate refuses bad answers." | It refuses only what it can prove wrong. Withholding is enabled on **BLOCKED only**, which was **2 rows of 243** production rows. FLAGGED rows are advisory and still shown. |
| "This is an accuracy rate." | There is **no accuracy rate here.** A 12-case regression benchmark matched expectations on 12 of 12 cases, 6 of them exactly. Two case labels were corrected the same day. Twelve cases is a demonstration, not a rate. |
| "Three independent parties agreed." | **One custodian holds all three signing keys** in the current research posture. A 2-of-3 quorum here certifies that one principal drove three seat identities over the same bytes. It is never independent agreement. |
| "The record is complete." | Only a minority of replies carry a verdict at all. Rows that could not be checked say `NOT_CHECKED`. That is a documented gap, not a clean result. |

If a later entry contradicts a line in this table, the contradiction is the finding, and the entry
says which line it supersedes.

## What this record will never contain

These are hard exclusions, enforced by a gate that runs before every commit. A tree that fails the
gate does not publish.

- **No conversations.** Not a reply, a prompt, a transcript, or a summary of one. No message text of
  any kind.
- **No code.** No engine source, scripts, site assets, notebooks, or configuration that executes.
- **No personal data.** No names beyond an approved byline, no addresses, no contact details, no
  financial records, no health records, no network or location identifiers, no credentials.
- **No customer or client material.** No names, tenants, or contact details of any organisation.

## What a row contains

A row records a check, not a conversation: a sequence number, a timestamp, a verdict, which rules
ran and which did not, and a hash linking it to the row before it. Text from any input is never
stored, only the verdict and the shape of what was checked.

Every row carries `is_sample`. A synthetic fixture and a production observation can never be
confused, and a row that does not declare which it is does not publish.

## How to check it without trusting it

The record is hash-chained. Each row carries a digest over its own content and the digest of its
predecessor, so a rewritten row breaks the chain at that point and every row after it. You do not
need to trust the operator, the vendor, or this README: recompute the chain from the rows.

A break, a gap, or a duplicate sequence number is a finding. Report it.

## Scope

This repository holds record data and prose only. It is not the product, not the engine, and not a
statement that any system is ready for use. The commercial system is separate and is not published
here.
