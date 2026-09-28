# Calvin Tjoaquinn

Security research on machine-generated code: how it fails, how to measure the
failures, and how to build environments that verify a model actually found the bug
instead of describing one.

## What I work on

**[solexploit-gen](https://github.com/CalvinTjoaquinn/solexploit-gen)** — a generative
smart-contract exploitation environment. A parametrized generator injects a
decoy-obscured Solidity vulnerability into a fresh contract; the model writes an
exploit; the exploit is deployed on a bare anvil node and graded by whether the
protocol invariant actually broke. Binary reward from real EVM execution, no LLM
judge in the loop. Four vulnerability classes (reentrancy, access control, price
oracle, signature replay), deterministic per seed. `MIT`

**[hallusec-replication](https://github.com/CalvinTjoaquinn/hallusec-replication)** —
replication package for *Detecting Security-Critical Code Hallucinations in
LLM-Generated Code*. `MIT`

Day to day I read other people's code looking for the specific place where a
security assumption stops holding — access-control checks that run after the state
change, parsers that trust a length field, auth paths that validate the wrong
object. Most of my public contributions come out of that habit.

## Upstream contributions

Merged pull requests to repositories I don't own:
[all PRs](https://github.com/pulls?q=is%3Apr+author%3ACalvinTjoaquinn+is%3Amerged+sort%3Aupdated-desc)

I work on agent tooling, security rule sets, and LLM evaluation harnesses. If one
of my patches touches your project and you want it split, rebased, or backed by a
regression test, open a comment on the PR and I will follow up.

## Interests

Verifiable rewards for security tasks · virtio / hypervisor attack surface ·
static analysis rules · LLM evaluation that resists contamination

Student, based in Indonesia. Reachable through GitHub issues on any of the repositories above.
