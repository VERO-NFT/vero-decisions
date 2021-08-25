# VERO Decisions

This repository contains all the decisions around the approval, rejection, or revocation of VEROs. The working idea for
the process is that after a new token is minting against the VERO smart contract, the VERO information will be posted
here as a new pull request to gather community feedback on whether the token meets all the criteria to become a VERO.
After a period of time and debate, a decision will be made, which is reflected as a commit to the pull request and will
be merged into the main branch effectively codifying the decision.

# Why here? Why in this way?

Decisions should be transparent and exist indefinitely without the need for exclusive access to get the details that may
be important to you. Recording those decisions shouldn't be overly burdensome else the people making the decisions will
decide to take an easier route - not doing it. In the software development world, there is a streamlined process for
recording decisions called *Architectural Decision Records*, or *ADRs*. ADRs are lightweight, point-in-time records of a
decision and the surrounding context that others understand why it was made. This is very much the same time of
rationale that we want to record with decisions around approving, rejecting, or revoking VEROs.

If you're interested in reading a well-conceived article around applying ADRs to all types of decisions, which inspired
me to apply them here, read this article (2nd part) from [Olaf Zimmermann](https://ozimmer.ch/about/) titled
["ADR = Any Decision Record?"](https://medium.com/olzzio/adr-any-decision-record-916d1b64b28d).

# Requirements

* Node 12 or 14

# Steps to create decision record and record the decision

1. Run `npm install` from the repo root folder.
2. Create a new branch off of the `main` branch. For VERO status decisions, ideally include the token ID in the branch
   name.
3. Copy the decision record template file, `template.md`, and paste the file with a new name into the `decisions`
   folder. Follow the file name conventions for the project, which are as follows:
    1. Use the next number in the decision record sequence, e.g., `000034`.
    2. If for a decision on the status of a VERO, include the token ID after the word `token`, e.g., `token27`.
    3. Example of the decision record name for a VERO: `000034-token27.md`.
4. Update the new decision record with as many relevant details as possible. Reflect the best encapsulation of the
   factors in play that led to the decision. Follow the clues present in the template file to guide how the decision is
   recorded. The best advice to use is to be honest and clear.
5. Run `npm run update_adr` to refresh the decision records list in the `decisions` folder.
6. Commit your changes and push up the branch. Create a pull request (PR) with the new decision branch changes.
7. After approval and merging of the PR, the VERO will be updated on the blockchain to the status reflected in the
   decision record, if it was related to a VERO. This step is done manually right now by the VERO Admin Account but may
   be automated in the future.