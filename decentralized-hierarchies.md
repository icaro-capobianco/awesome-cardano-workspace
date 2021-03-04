This is a proposal I had submitted for Catalyst F4: Distributed Decision Making, but since I submitted it a bit too late I decided to put it here so people can see it.

# Idea: decentralized hierarchies

## Problem statement :
Decentralization is not enough to make good decisions, some sort of hierarchy is necessary, but that doesn't mean it can't be decentralized.

## Describe your solution to the problem
My proposal is what I call a "recursive hierarchy", which would allow a very flexible hierarchy based on votes and rights.

## Relevant experience
I'm just a self taught programmer, I've been working as a freelancer for 3 years now and I believe I had a very good career so far.

# Detailed plan

**Describing a scenario**

Charles creates a group, when he does it he has all the rights, including the right to invite others(1), so he invites James, then Charles also gives James the right to invite people(2), then James invites Bob, and now Charles decides that in order to invite more people, a poll needs to be made, so he gives James and Bob the right to vote(3) and the right to poll an invitation (4), then he revokes the right to invite without a poll (5).

**Analyzis**

- 1 - Right to Invite
- 2 - Right to grant the right to Invite
- 3 - Right to vote on poll to Invite
- 4 - Right to create poll to Invite
- 5 - Right to revoke right to Invite

Now replace Invite with X

 - Right to X
 - Right to grant the right to X
 - Right to vote on poll X
 - Right to create poll X
 - Right to revoke right to X

**Recursion**

"Right to grant right to vote on poll to vote on poll to create poll to revoke right to Invite"

Complex recursion is solved with a DSL and good UI.

**Roles**

Roles group rights, adding a bit more complexity

 
Replace the X above with each of these:

- Assign Role
- Revoke Role

Rights are assigned to roles in the same way they are assigned to users. (This can be problematic so it needs more thought)

**Meritocracy**

Roles can group rights based on a meaningful quality, for example:

- Designer: Right to vote on X
- Developer: Right to vote on Y
- Economist: Right to vote on Z
- Engineer: Right to vote on XYZ

**Vote Weight, the solution to not exclude people**

Replace all the cases where you saw "vote on X" with:
Vote on X with weight N ( 0 < N >= 1 )

Now everyone can vote on an engineering related poll, but the ones with the Engineer role may have a heavier vote weight.

## What is the point?

I described this system that is supposed to be very flexible and allow for many types of power structures to be created. What is great about it is that I am not telling you how to distribute power, because I actually don't know the solution for that, and I doubt anyone does. Some things work for some people, but not for others. What I am doing is providing tools to create a variety of power structures.

With a system like this, if 100000 people are divided among 100 groups of 1000, they may try 100 different combinations and that increases the chance of something that is better to arrive.

This is a very generic solution that can be applied to many cases, including to Cardano's distributed decision making.

## Implementation and Integrations

I'd love to see something like this being built on Haskell or F# or some awesome functional programming language.
I imagine it having plugins made by developers to create rights that interact with the outside world, for example: a plugin that provides the right to make a purchase with the money shared by the group, or to vote on those expenses, etc etc…

 

# Final thoughts

This is an idea I worked on my head throughout the last year, so maybe it's all wrong and I am just tripping on my own imagination. Anyway, if the value that I see in this idea is real and not just fantasy I would be happy to see further discuss and even work on implementing it.

**Requested funds in USD**
0, it's more for discussion

**Which of these definitions apply to you?**
- Developer
- Entrepreneur
