<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/osverify-dark.png">
    <img alt="OSVerify" src="assets/osverify-light.png" width="420">
  </picture>
</p>

<p align="center"><b>One-sided verification under limited expert review</b></p>

AI has become increasingly helpful in scientific discovery, yet problems without reliable
automated evaluation still depend on human expert review, and candidate generation now
scales far beyond the review capacity available. We study verification under limited
human effort: rare valid solutions should reach experts first, and invalid candidates
should be filtered out to reduce their workload.

OSVerify adopts a one-sided objective. It maximizes the rejection rate of invalid
solutions while keeping the false-rejection rate of valid ones under a fixed limit, which
makes the cost of human review an explicit quantity to minimize. Since verifying a
specific error is often easier than discovering one, OSVerify decouples error proposal
from error validation. The proposer searches for errors at different granularities by
hierarchical decomposition, and the validator separates substantial errors from minor or
hallucinated ones.

On competition- and research-level benchmarks, OSVerify reduces the number of human
reviews of invalid solutions by 46% on average compared with voting baselines at the same
low false-rejection rate, and post-training the validator raises the reduction to 57%. It
has found errors in published research papers that were confirmed by their authors, and
it has helped resolve open conjectures whose proofs were confirmed by experts.

- [OSVerify](https://github.com/OSVerify/OSVerify): the verifier, for solutions and
  research papers, with an agent skill.
- [Rethlas-OSV](https://github.com/OSVerify/Rethlas-OSV): Rethlas proof generation
  reviewed by OSVerify, with a desktop app (beta).
- [Website](https://osverify.github.io)
