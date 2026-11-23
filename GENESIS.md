# Genesis — day zero

**Opened: 2026-11-22.** This entry is row zero of the record. Everything that follows is appended
after it.

## The boundary of this record

This record begins here. It imports nothing from any earlier record and describes nothing that
happened before this commit. The boundary is deliberate: a reader can recompute every row in this
repository from the rows themselves, and never has to take an operator's word for what came before.

That rule extends to numbers. Any figure stated in this repository is computed from rows in this
repository. A figure that cannot be recomputed here is not stated here.

## The rules of this record

These take effect at launch. The commit that writes row one is the boundary.

1. **Append only, from launch.** Until row one exists, this record is being assembled and may be
   corrected freely. From the first row onward, a dated entry is never edited, and a correction is a
   new entry naming what it supersedes. A back-changed record is worth nothing, which is why the
   lock starts when the data does.
2. **One writer.** A single process appends. Concurrent writers are not permitted, because after the
   fact a fork is indistinguishable from a tamper attempt.
3. **Every row declares itself.** `is_sample` is required and boolean. There is no default, and a row
   that does not declare whether it is synthetic does not publish.
4. **Nothing is stored that could expose a person.** Verdicts and check outcomes are stored. Input
   text is not. No names, no contact details, no locations, no credentials.
5. **The gate runs before the commit.** A tree that fails the content gate does not publish, and a
   skipped scan counts as a failed scan.
6. **A gap is stated, not hidden.** A row that could not be checked says so. Coverage is reported
   with the same prominence as any success.

## What row one will be

The first row is the first check the single writer performs against a synthetic input after this
genesis. It carries its own `is_sample: true`, its verdict, which rules ran and which did not, and
its hash link back to this genesis.

No row is backfilled and no earlier data is imported. The record is what happened after this commit.

## What this record is not

It is not a claim that any system is correct, safe, or ready for use. It is not a benchmark result
and it is not a certification. It is a hash-chained account of what one deterministic check did to
one synthetic input at a stated time, written so that a party who trusts neither the operator nor
the vendor can recompute it and disagree.

*Prototype, research and educational use only. Licence CC BY-NC-ND 4.0.*
