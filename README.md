# Iscandar — edit history

The stacked source history of "An Extension of Buddy Systems to Arbitrary
Radix for Deterministic Memory Allocation," oldest version first, one
commit per version, so the development can be reviewed diff by diff.
Copied from the author's Overleaf projects and his email escrows on
2026-10-22.

## How to read this history

Ordering is the reverse of the Overleaf project-list order (the list runs
most-recently-modified first), so the chain reads oldest first. Each
Overleaf version is one commit whose tree is that version's source.
Versions that also exist as dated email escrows carry the compiled PDF
under `pdf/` in the same commit and a git tag with the version number.
Versions that exist only as email escrows appear as their own commits,
dated with the email's date, carrying the source tree forward and adding
their PDF. Versions with no escrow PDF carry source only: the chain
documents every state, including versions that were never compiled to
PDF. A version whose source is byte-identical to its predecessor's is
recorded in MANIFEST.json as checkpoint-identical instead of getting an
empty commit.

## Authorship

The paper was hand-assembled by the author with cut and paste. Gemini
assisted with literature search, grammar, and organizing. The argument
and the assembly are the author's.

## Design intent

The unrolled fixed-width drivers are a specification for parallel silicon
for the time being: in hardware each level's scan is parallel comparators
firing in one cycle, the k×A bound reads as pipeline depth, and the
software is the specification model until silicon exists.
