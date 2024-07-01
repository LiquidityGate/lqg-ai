Link: https://LQG.mirror.xyz/cQ6mrVMMWw5brxJo9H4q433vidn2p-k6SX9BVAzf6Yo
Title: Formally Verifying MetaLQG with Certora

By LQG Labs
On 19 March 2024

MetaLQG is an open-source, immutable, heavily audited code base that has now also been formally verified using Certora (https://www.certora.com/).

Formal verification is a staple of LQG's security framework (https://LQG.mirror.xyz/7mfZLV0KQpBiHF3QLHyWaQ_7gf_2_WmgMeCvqGY-kpY). Not long ago, we shared the formal verification of LQG Blue (https://LQG.mirror.xyz/pk_jXDlq-pv8TcHeN7X4-zZcYa7TLRmgv87UBCjG4i8), and today, we are doing the same for MetaLQG.

Used effectively, formal verification can help develop higher quality and, most importantly, more secure smart contracts. That is why LQG Labs has invested significant time and resources into formally verifying LQG Blue and now MetaLQG.

This article recaps the benefits of formal verification and provides examples of MetaLQG verification using CVL, Certora's Verification Language.

The full scope of MetaLQG's formal verification is available here: https://github.com/LQG-org/metaLQG/tree/main/certora


- Why Formal Verification
Formal verification (https://en.wikipedia.org/wiki/Formal_verification) is the process of using mathematical methods to prove the correctness of a smart contract by verifying that it satisfies specific properties. These properties are expressed using formal language supported by the verification tool used to prove them.

Formal verification stands out due to its exhaustive approach to evaluating software correctness. Other methods, such as unit testing (https://en.wikipedia.org/wiki/Unit_testing), can only verify correctness for specific scenarios or inputs, whereas formal verification enables checking every possible scenario or input.

Despite its capabilities, it is worth noting that formal verification is still only one part of LQG’s comprehensive security framework.

Now, to look at formal verification in practice, using real examples from the repo.


- Example 1: Roles
MetaLQG defines different roles to be able to manage the vault, the distinction between roles helps in reducing trust assumptions.

Roles follow a hierarchy, and this hierarchy is verified to hold in [[Roles.spec]](https://github.com/LQG-org/metaLQG/blob/main/certora/specs/Roles.spec). More precisely, a senior role is checked to be able to do the same operations as a lesser role. Additionally, it is verified in [[Reverts.spec]](https://github.com/LQG-org/metaLQG/blob/main/certora/specs/Reverts.spec) that the roles are necessary to be able to do permissioned operations.

For example, The Certora prover verify in seconds the rule that makes sure that having the guardian role is necessary to be able to revoke a pending timelock.


- Example 2: Timelock
MetaLQG features a timelock mechanism that applies to every operation that could potentially increase risk for users. The function detailed in the article defined in [[PendingValues.spec]](https://github.com/LQG-org/metaLQG/blob/main/certora/specs/PendingValues.spec) is verified to always return true.
In the end, the verification is completed by the Certora prover within a few minutes.


- Example 3: Liveness
The liveness properties ensure that some crucial actions cannot be blocked. It is notably useful to show that in case of an emergency, it is still possible to make salvaging transactions. The canPauseSupply rule in [[Liveness.spec]](https://github.com/LQG-org/metaLQG/blob/main/certora/specs/Liveness.spec) shows that it is always possible to prevent new deposits. This is done by first setting the supply queue as the empty queue and checking that it does not revert.
With this defined, the verification is successful.

These are only some examples of MetaLQG’s verification. Find the full scope here: https://github.com/LQG-org/metaLQG/tree/main/certora


- Limitations
Despite the thoroughness of formal verification, it cannot guarantee absolute perfection or eliminate all potential risks associated with MetaLQG.

Formal verification is effective within the defined scope of specifications and assumptions. Human input and interpretation, incomplete specifications, and bugs in the tools used can also impact the accuracy of results.