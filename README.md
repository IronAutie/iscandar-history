# Iscandar — edit history

The stacked source history of "An Extension of Buddy Systems to Arbitrary
Radix for Deterministic Memory Allocation," oldest version first, one
commit per version, so the development can be reviewed diff by diff.
Copied from the author's Overleaf projects and his email escrows on
2026-10-22.

**Read the paper:** [Iscandar-24c.pdf](Iscandar-24c.pdf) is the compiled PDF of the newest version (24c), rendered by Overleaf on 2026-10-22. Its source is `main.tex` at the tip of this history.

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

## Provenance

This allocator was first designed in 1998, as proprietary industry work.
It was developed without access to the published literature, and it was
never published: when the author walked away, the work stayed behind.
What survived was the author's memory of the design, including its
drawings, kept from 1998 onward. In 2026, the copyright in the original
work having lapsed, the author reconstructed the design from memory; the
paper and this history are that reconstruction. Similarities to
published work the author had not seen, such as Brent (1989), are
independent invention. The 1998 design predates the closest later works
(Agun & Chang 2003; TLSF 2004), and the reconstruction borrows from
none of them: it descends from the 1998 design alone.

## Note on independence

This design was developed in 1998 as proprietary industry work,
without access to the published literature, and was reconstructed from
the author's memory in 2026, after the copyright in the original work
had lapsed. Parts of it therefore duplicate published results
independently: non-binary buddy variants (Peterson and Norman, 1977),
aggregate-steered tree allocation (Brent, 1989), search-free placement
at the price of incomplete memory use (Ogasawara, 1995; Masmano et
al., 2004, 2008), and buddy allocation in hardware (Agun and Chang,
2003); see also the survey of Wilson et al. (1995). The duplication is
independent in both directions: the author had seen none of the
earlier work, and the 1998 design predates the closest later work.
Similarities to the works cited are independent duplication, not
derivation.

## Design intent

The unrolled fixed-width drivers are a specification for parallel silicon
for the time being: in hardware each level's scan is parallel comparators
firing in one cycle, the k×A bound reads as pipeline depth, and the
software is the specification model until silicon exists.
