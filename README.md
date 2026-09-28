# Calvin Tjoaquinn

Security research on machine-generated code. How it fails, and how to build
environments that verify a model actually found the bug instead of describing one.

## What I work on

**[solexploit-gen](https://github.com/CalvinTjoaquinn/solexploit-gen)** is a generative
smart-contract exploitation environment. A parametrized generator injects a
decoy-obscured Solidity vulnerability into a fresh contract, the model writes an
exploit, and the exploit runs on a bare anvil node where the reward is whether the
protocol invariant actually broke. No LLM judge in the loop. Four vulnerability
classes, deterministic per seed. `MIT`

**[virtio-fuzz-ci](https://github.com/CalvinTjoaquinn/virtio-fuzz-ci)** runs the
upstream `cargo-fuzz` targets for the rust-vmm virtio parsers on GitHub-hosted
runners, with the corpus cached between runs so coverage compounds. `MIT`

**[hallusec-replication](https://github.com/CalvinTjoaquinn/hallusec-replication)** is the
replication package for *Detecting Security-Critical Code Hallucinations in
LLM-Generated Code*. `MIT`

## Upstream contributions

Most of what I send upstream starts from using a tool rather than reading its issue
tracker. A recent example: `forge fmt` asserts internally that formatting twice
gives the same output, but the CLI path skips that check, so I formatted 9,726
Solidity files from ten repositories twice and compared. Ten diverged, which
reduced to seven distinct causes, two of which moved a comment onto a different
construct than the author attached it to.

- [foundry-rs/foundry#17107](https://github.com/foundry-rs/foundry/issues/17107),
  the report, with a minimal reproduction per cause
- [foundry-rs/foundry#17108](https://github.com/foundry-rs/foundry/pull/17108),
  merged, stops a Yul block being inlined when the statement inside it always breaks
- [All merged PRs](https://github.com/pulls?q=is%3Apr+author%3ACalvinTjoaquinn+is%3Amerged+sort%3Aupdated-desc)

If a patch of mine touches your project and you want it split differently or backed
by a regression test, say so on the PR and I will follow up.

## Interests

Verifiable rewards for security tasks · virtio and hypervisor attack surface ·
LLM evaluation that resists contamination

Student, based in Indonesia. Reachable through GitHub issues on any repository above.
