# Voting

[What gets voted on at Ajna?](voting.md#what-gets-voted-on-at-ajna)\
[How does the voting system work?](voting.md#how-does-the-voting-system-work)\
[What is the screening stage?](voting.md#what-is-the-screening-stage)\
[What is the funding stage?](voting.md#what-is-the-funding-stage)\
[What is the challenge stage?](voting.md#what-is-the-challenge-stage)\
[What proposals are voted on in the funding stage?](voting.md#what-proposals-are-voted-on-in-the-funding-stage)\
[Is there a minimum number of funding stage votes for a proposal to be funded?](voting.md#is-there-a-minimum-number-of-funding-stage-votes-for-a-proposal-to-be-funded)\
[How are votes counted and is there a required quorum?](voting.md#how-are-votes-counted-and-is-there-a-required-quorum)\
[Who is eligible to participate in the voting process?](voting.md#who-is-eligible-to-participate-in-the-voting-process)\
[Can I delegate my voting power?](voting.md#can-i-delegate-my-voting-power)\
[How do I submit a proposal?](voting.md#how-do-i-submit-a-proposal)\
[What is Quadratic Voting?](voting.md#what-is-quadratic-voting)\
[Why is Quadratic Voting only used in the Funding Round?](voting.md#why-is-quadratic-voting-only-used-in-the-funding-round)\
[How often are votes held?](voting.md#how-often-are-votes-held)\
[How long do participants have to cast their votes in the screening stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-screening-stage)\
[How long do participants have to cast their votes in the funding stage?](voting.md#how-long-do-participants-have-to-cast-their-votes-in-the-funding-stage)\
[Can I change my vote after it’s been cast?](voting.md#can-i-change-my-vote-after-its-been-cast)\
[Can participants propose changes to the voting system?](voting.md#can-participants-propose-changes-to-the-voting-system)\
[Are there any incentives for participating?](voting.md#are-there-any-incentives-for-participating)\
[What happens if a proposal is passed but is not technically feasible?](voting.md#what-happens-if-a-proposal-is-passed-but-is-not-technically-feasible)\
[Can the voting system be used to amend the protocol's smart contracts?](voting.md#can-the-voting-system-be-used-to-amend-the-protocols-smart-contracts)\
[Can a proposal be resubmitted?](voting.md#can-a-proposal-be-resubmitted)

### What gets voted on at Ajna?

Grant applications. That's it.

### How does the voting system work?

Ajna's voting system has three stages.\
The first is a screening stage which runs for 73 days and counts 1 token = 1 vote.\
The second is a funding stage which runs for 10 days and uses a quadratic system for votes.\
The third is a challenge stage which runs for 7 days and allows anyone to propose alternative payout configurations that might be more optimal.

<figure><img src="../.gitbook/assets/Flowcharts - Plan, do, check, act (6) (1).png" alt=""><figcaption><p>Voting Cycle Stages</p></figcaption></figure>

For more detail review sections 9.2.1 in the whitepaper.

### What is the screening stage?

The screening stage is for voters to filter out the proposals they are not interested in funding. The Screening stage runs for 73 days and counts 1 token = 1 vote. An uncapped number of proposals can be submitted, but only the top 10 move on.

### What is the funding stage?

The funding stage is the second stage of the voting cycle which runs for 10 days and uses a quadratic system for votes. The top 10 proposals from the screening stage advance to the funding stage where they may receive both positive and negative votes in a quadratic manner; Meaning the number of voting credits they have increases with the number of proposals they vote on (see image below).

<figure><img src="../.gitbook/assets/Cumulative Voting Power vs. Number of Proposals Voted On (2).png" alt=""><figcaption></figcaption></figure>

### What is the challenge stage?

After the Funding Stage concludes, there is a one-week challenge stage where alternative sets of winning proposals can be submitted. During this time, the optimal batch of proposals is selected by considered factors such as budget constraint and votes received. If a new batch is submitted that is just as optimal as the current one, than the current one stays in place.

### What proposals are voted on in the funding stage?

Only the top 10 proposals from the screening stage can be voted on in the funding stage.

### How are votes counted and is there a required quorum?

Screening stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the screening stage’s start block, where one token is equal to one vote. \
\
Funding stage: Voting power is based upon a snapshot of an address' voting power 33 blocks prior to the funding stage's starting block, and uses a quadratic system.\
\
Challenge stage: There is no voting during the challenge stage. Rather, anyone can submit an alternative optimal set of results from the funding stage.\
\
There are no quorums.

### Who is eligible to participate in the voting process?

One must either have AJNA tokens or be delegated AJNA tokens to vote.

### Can I delegate my voting power?

Yes.

### How do I submit a proposal?

One way to submit a proposal is through the Ajna Voting App.

### What is Quadratic Voting?

Quadratic voting is a system that allows individuals to express their preferences using a budget of voting points. Unlike traditional "one person, one vote" systems, individuals can allocate their voting points based on the importance of the issue to them, giving more weight to their individual opinions. The allocation of voting points follows a quadratic function, which means that the number of voting points increases as more items are voted on. This system incentivizes people to vote on all items and can lead to a more accurate and nuanced representation of individual opinions.

### Why is Quadratic Voting only used in the funding stage?

The screening stage allows unlimited entries, which breaks quadratic voting due to the way voting credit is counted.

### Is there a minimum number of funding stage votes for a proposal to be funded?

Proposals with 0 or negative votes in the funding stage will not be eligible for funding.

### How often are votes held?

Each cycle runs for 90 days and has three stages. \
The first is a screening stage which runs for 73 days.\
The second is a funding stage which runs for 10 days.\
The third is a challenge stage which runs for 7 days.\
\
Votes can be submitted at at any time, but may not be modified.

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

