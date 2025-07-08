# Implementation Status

Note to RFC Editor: Please remove this section as well as references to BCP205 before AUTH48.

This section records the status of known implementations of the protocol defined by this specification at the time of posting of this Internet-Draft, and is based on a proposal described in BCP205.
The description of implementations in this section is intended to assist the IETF in its decision processes in progressing drafts to RFCs.
Please note that the listing of any individual implementation here does not imply endorsement by the IETF.
Furthermore, no effort has been spent to verify the information presented here that was supplied by IETF contributors.
This is not intended as, and must not be construed to be, a catalog of available implementations or their features.
Readers are advised to note that other implementations may exist.

According to BCP205,
"this will allow reviewers and working groups to assign due consideration to documents that have the benefit of running code, which may serve as evidence of valuable experimentation and feedback that have made the implemented protocols more mature.
It is up to the individual working groups to use this information as they see fit".

## Implementers

### DataTrails

An open-source implementation was initiated and is maintained by Data Trails Inc. - DataTrails.

Uses SHA-256 as the hash alg

#### Implementation Name

An application demonstrating the concepts is available at [https://app.datatrails.ai/](https://app.datatrails.ai/).

#### Implementation URL

An open-source implementation is available at:

- <https://github.com/datatrails/go-datatrails-merklelog>

#### Maturity

Used in production.
SEMVER unstable (no backwards compat declared yet)

### Robin Bryce (1)

#### Implementation URL

A minimal reference implementation of this draft.
Used to generate the test vectors in this draft, is available at:

- <https://github.com/robinbryce/draft-bryce-cose-merkle-mountain-range-proofs/blob/main/algorithms.py>

#### Maturity

Reference only

### Robin Bryce (2)

#### Implementation URL

A minimal tiled log implementation

- <https://github.com/robinbryce/mmriver-tiles-ts>

#### Maturity

Prototype

### Mimblewimble

Is specifically committing to positions as we describe, but is committing zero based indices,
and uses BLAKE2B as the HASH-ALG.
Accounting for those differences, their commitment trees would be compatible with this draft.

#### Implementation URL

An implementation is available here:

- <https://github.com/mimblewimble/grin/blob/master/doc/mmr.md> (Grin is a rust implementation of the mimblewimble protocol)
- <https://github.com/BeamMW/beam/blob/master/core/merkle.cpp> (Beam is a C++ implementation of the mimblewimble protocol)

###  Herodotus

#### Implementation URL

<https://github.com/HerodotusDev/rust-accumulators>

Production, supports keccak, posiedon & pedersen hash algs

Editors note: test vectors, based on a SHA256 instantiation, are currently provided in a separate document.
These should inlined if the draft is accepted: <https://github.com/robinbryce/draft-bryce-cose-merkle-mountain-range-proofs/blob/main/test-vectors.md>