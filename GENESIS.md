# Genesis — day one

**Opened: 2026-11-22.** This entry is row zero of the record. Everything that follows is appended
after it and nothing before it is rewritten.

## Why this record starts empty

An earlier record existed and it taught three lessons that are cheaper to honour than to fix:

1. **Two writers produce forks.** Two systems appending to one chain created repeated sequence
   numbers at three points. A reader cannot tell a fork from a tamper attempt after the fact. This
   record has one writer.
2. **An unlabelled fixture is a lie waiting to be told.** Rows written during testing were once
   indistinguishable from production observations. Every row here carries `is_sample`.
3. **A published mistake cannot be retracted.** A redaction after publication leaves the original
   downloadable. The gate runs before the commit, never after.

Starting from zero avoids all three by construction rather than by discipline.

## The rules of this record

1. **Append only.** A dated entry is never edited. A correction is a new entry naming what it
   supersedes.
2. **One writer.** A single process appends. Concurrent writers are not permitted, because a fork
   is indistinguishable from tampering after the fact.
3. **Every row declares itself.** `is_sample` is required and boolean. There is no default.
4. **Nothing is stored that could expose a person.** Verdicts and check outcomes are stored. Input
   text is not.
5. **The gate runs before the commit.** A tree that fails the content gate does not publish, and a
   skipped scan is a failed scan.
6. **A gap is stated, not hidden.** A row that could not be checked says so. Coverage is reported
   with the same prominence as any success.

## What row one will be

The first row is the first check performed by the single writer against a synthetic input after this
genesis commit. It will carry its own `is_sample: true`, its verdict, which rules ran, which did not,
and its hash link to this genesis.

No row is backfilled, and no earlier data is imported. The record is what happened after this
commit, and it says nothing about anything that happened before it.

## What this record is not

It is not a claim that any system is correct, safe, or ready for use. It is not a benchmark result.
It is not a certification. It is a hash-chained account of what one deterministic check did to one
synthetic input at a stated time, written so that a party who trusts neither the operator nor the
vendor can recompute it and disagree.

*Prototype, research and educational use only. Licence CC BY-NC-ND 4.0.*
