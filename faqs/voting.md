# Voting

[What gets voted on at Ajna?](voting.md#what-gets-voted-on-at-ajna)\
[How does the voting system work?](voting.md#how-does-the-voting-system-work)\
[How are votes counted and is there a required quorum?](voting.md#how-are-votes-counted-and-is-there-a-required-quorum)\
[Who is eligible to participate in the voting process?](voting.md#who-is-eligible-to-participate-in-the-voting-process)\
[Can I delegate my voting power?](voting.md#can-i-delegate-my-voting-power)\
[How can I submit a proposal?](voting.md#how-can-i-submit-a-proposal)\
[What is Quadratic Voting?](voting.md#what-is-quadratic-voting)\
[Why is Quadratic Voting only used in the Funding Stage and not the Screening Stage as well?](voting.md#why-is-quadratic-voting-only-used-in-the-funding-round-and-not-the-screening-stage-as-well)\
[How often are votes held?](voting.md#how-often-are-votes-held)\
[How long do participants have to cast their votes in the screening stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-screening-stage)\
[How long do participants have to cast their votes in the funding stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-funding-stage)\
[Can I change my vote after it’s been cast?](voting.md#can-i-change-my-vote-after-its-been-cast)\
[Can participants propose changes to the voting system?](voting.md#can-participants-propose-changes-to-the-voting-system)\
[Are there any incentives for participating?](voting.md#are-there-any-incentives-for-participating)\
[What happens if a proposal is passed but is not technically feasible?](voting.md#what-happens-if-a-proposal-is-passed-but-is-not-technically-feasible)\
[Can the voting system be used to amend the protocol's smart contracts?](voting.md#can-the-voting-system-be-used-to-amend-the-protocols-smart-contracts)\
[Can a proposal be resubmitted?](voting.md#can-a-proposal-be-resubmitted)\
[What is the challenge period?](voting.md#what-is-the-challenge-period)\
[Can a new vote cycle start during the challenge period?](voting.md#can-a-new-vote-cycle-start-during-the-challenge-period)

### What gets voted on at Ajna?

Voting relates to the approval or disapproval of grant applications. That's it.

### How does the voting system work?

Ajna has two voting mechanisms. \
The Primary Funding Mechanism (PFM) and the Extraordinary Funding Mechanism (EFM)\
\
Under normal circumstances, the PFM is used.\
Under extraordinary circumstances, the EFM is used. \
\
The PFM has two stages and a challenge period at the end of each cycle.\
The first is a screening stage which runs for 80 days and counts 1 token = 1 vote.\
The second is a funding stage which runs for 10 days and uses a quadratic system that counts x tokens = x^2 votes.\
The challenge period begins at the end of the funding stage, lasts 7 days, and allows anyone to propose a different configuration for payouts.\
\
The EFM has one phase which runs for one month and counts 1 token = 1 vote.\
Votes can only be cast in support of the proposal. The amount of requested funds determines the required quorum. The result is pass or fail.\
\
For more detail review sections 9.2.1 and 9.2.2 in the whitepaper.

### How are votes counted and is there a required quorum?

Votes are counted in different ways depending on the voting mechanism and stage. \
\
PFM screening stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the screening stage’s start block, where one token is equal to one vote. \
PFM funding stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the funding stage's starting block, and uses a quadratic system.\
\
Quorum is only required in the EFM and depends on the amount of funds being asked for.

### Who is eligible to participate in the voting process?

To vote one must either have AJNA tokens or be delegated AJNA tokens.

### Can I delegate my voting power?

Yes.

### How can I submit a proposal?

1. Forum
2. On-chain[Track package](https://www.amazon.com/progress-tracker/package/ref=ppx\_yo\_dt\_b\_track\_package?\_encoding=UTF8\&itemId=pnjimqhmpjpron\&orderId=114-3467708-1733014\&vt=YOUR\_ORDERS)

### What is Quadratic Voting?

Quadratic voting is a system that allows individuals to express their preferences using a budget of voting points. Unlike traditional "one person, one vote" systems, individuals can allocate their voting points based on the importance of the issue to them, giving more weight to their individual opinions. The allocation of voting points follows a quadratic function, which means that the cost of allocating additional voting points to a single issue increases as more voting points are allocated to that issue. This system incentivizes people to vote on the issues they care about most and can lead to a more accurate and nuanced representation of individual preferences, particularly on complex or controversial issues.

### Why is Quadratic Voting only used in the Funding Round and not the Screening Stage as well?

AAA

### How often are votes held?

Each cycle runs for 90 days and has two stages. \
The first is a screening stage which runs for 80 days.\
The second is a funding stage which runs for 10 days.\
Votes can be submitted at at any time.

### How long do participants have to cast their votes in the screening stage?

80 days. Votes cannot be cancelled or modified.

### How long do participants have to cast their votes in the funding stage?

10 days. Votes cannot be cancelled or modified.

### Can I change my vote after it’s been cast?

No, votes cannot be cancelled or modified.

### Can participants propose changes to the voting system?

No.

### Are there any incentives for participating?

Yes, delegates earn 10% of the AJNA distribution per cycle.

### What happens if a proposal is passed but is not technically feasible?

Then the AJNA tokens are still distributed and the protocol funded something it should not have funded. This would be a failure of due diligence on the part of voters.

### Can the voting system be used to amend the protocol's smart contracts?

No.

### Can a proposal be resubmitted?

Proposals can be resubmitted, there is no limitation on how many times.

### What is the challenge period?

When the funding stage ends, an automatic calculation happens to determine the winning group of proposals. There may be more than one valid configuration of the final winners, therefore this challenge period allows anyone to propose a different grouping.

### Can a new vote cycle start during the challenge period?

