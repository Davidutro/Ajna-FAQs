# Voting

[What gets voted on at Ajna?](voting.md#what-gets-voted-on-at-ajna)\
[How does the voting system work?](voting.md#how-does-the-voting-system-work)\
[What is the screening stage?](voting.md#what-is-the-screening-stage)\
[What is the funding stage?](voting.md#what-is-the-funding-stage)\
[What proposals can be voted on in the funding stage?](voting.md#what-proposals-can-be-voted-on-in-the-funding-stage)\
[How are votes counted and is there a required quorum?](voting.md#how-are-votes-counted-and-is-there-a-required-quorum)\
[Who is eligible to participate in the voting process?](voting.md#who-is-eligible-to-participate-in-the-voting-process)\
[Can I delegate my voting power?](voting.md#can-i-delegate-my-voting-power)\
[How can I submit a proposal?](voting.md#how-can-i-submit-a-proposal)\
[What is Quadratic Voting?](voting.md#what-is-quadratic-voting)\
[Why is Quadratic Voting only used in the Funding Round?](voting.md#why-is-quadratic-voting-only-used-in-the-funding-round)\
[How often are votes held?](voting.md#how-often-are-votes-held)\
[How long do participants have to cast their votes in the screening stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-screening-stage)\
[How long do participants have to cast their votes in the funding stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-funding-stage)\
[Can I change my vote after it’s been cast?](voting.md#can-i-change-my-vote-after-its-been-cast)\
[Is there a minimum number of funding stage votes for a proposal to be funded?](voting.md#is-there-a-minimum-number-of-funding-stage-votes-for-a-proposal-to-be-funded)\
[Can participants propose changes to the voting system?](voting.md#can-participants-propose-changes-to-the-voting-system)\
[Are there any incentives for participating?](voting.md#are-there-any-incentives-for-participating)\
[What happens if a proposal is passed but is not technically feasible?](voting.md#what-happens-if-a-proposal-is-passed-but-is-not-technically-feasible)\
[Can the voting system be used to amend the protocol's smart contracts?](voting.md#can-the-voting-system-be-used-to-amend-the-protocols-smart-contracts)\
[Can a proposal be resubmitted?](voting.md#can-a-proposal-be-resubmitted)\
[What is the challenge period?](voting.md#what-is-the-challenge-period)\
[Can a new vote cycle start during the challenge period?](voting.md#can-a-new-vote-cycle-start-during-the-challenge-period)

### What gets voted on at Ajna?

Grant applications. That's it.

### How does the voting system work?

Ajna's voting system has two stages and a challenge period.\
The first is a screening stage which runs for 80 days and counts 1 token = 1 vote.\
The second is a funding stage which runs for 10 days and uses a quadratic system for votes.\
The challenge period begins at the end of the funding stage, lasts 7 days, and allows anyone to propose a different configuration of payouts.

<figure><img src="../.gitbook/assets/Flowcharts - Plan, do, check, act (3).png" alt=""><figcaption><p>Primary Funding Mechanism Cycle</p></figcaption></figure>

For more detail review sections 9.2.1 in the whitepaper.

### What is the screening stage?

The screening stage is for voters to filter out the proposals they are not interested in funding. The Screening stage runs for 80 days and counts 1 token = 1 vote. An uncapped number of proposals can be submitted, but only the top 10 move on.

### What is the funding stage?

The funding stage is the second stage of the voting cycle which runs for 10 days and uses a quadratic system for votes. The top 10 proposals from the screening stage advance to the funding stage where they may receive both positive and negative votes in a quadratic manner; Meaning the number of voting credits they have increases with the number of proposals they vote on (see image below).

<figure><img src="../.gitbook/assets/Cumulative Voting Power vs. Number of Proposals Voted On (2).png" alt=""><figcaption></figcaption></figure>

### What proposals can be voted on in the funding stage?

Only the top 10 proposals from the screening stage can be voted on in the funding stage.

### How are votes counted and is there a required quorum?

Votes are counted in different ways depending on the voting mechanism and stage. \
\
PFM screening stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the screening stage’s start block, where one token is equal to one vote. \
PFM funding stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the funding stage's starting block, and uses a quadratic system.\
\
There are no required quorums.

### Who is eligible to participate in the voting process?

One must either have AJNA tokens or be delegated AJNA tokens to vote.

### Can I delegate my voting power?

Yes.

### How can I submit a proposal?

One way to submit a proposal is through the Ajna Voting App.

### What is Quadratic Voting?

Quadratic voting is a system that allows individuals to express their preferences using a budget of voting points. Unlike traditional "one person, one vote" systems, individuals can allocate their voting points based on the importance of the issue to them, giving more weight to their individual opinions. The allocation of voting points follows a quadratic function, which means that the number of voting points increases as more items are voted on. This system incentivizes people to vote on all items and can lead to a more accurate and nuanced representation of individual opinions.

### Why is Quadratic Voting only used in the funding round?

The screening stage allows unlimited entries, which breaks quadratic voting due to the way voting credit is counted.

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

### Is there a minimum number of funding stage votes for a proposal to be funded?

Proposals with 0 or negative votes in the funding stage will not be eligible for funding.

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

When the funding stage ends, a calculation must happen off-chain with a hash of the configuration submitted to the smart contract to determine the winning group of proposals. There may be more than one valid configuration of winners, therefore this challenge period allows anyone to propose a different grouping. Configurations may be submitted until the one week period is over, but there is a theoretically optimal configuration for any set of proposals that can be submitted at any time. If a new grouping is submitted that is just as optimal as the current one, than the current one stays in place.

### Can the next cycle's screening stage start during the challenge period?

Yes, a new cycle can start immediately after the conclusion of the funding stage.

