# ARLO AI — Deriv Hackathon concept

**A hackathon concept and evidence archive.** This repository documents the
ARLO AI dispute-resolution idea and the presentation materials supplied by the
team. The application source code is not available in this repository, and the
materials should not be read as proof of a deployed financial service.

## The challenge

At the February 2025 Deriv Hackathon, our team worked on the DP2P Automated
Dispute Resolution challenge. We designed ARLO AI as a chat assistant to help
review buyer–seller disputes, look for possible fraud signals, and guide a
resolution using transaction evidence.

**Team:** [Nur Ameera Chan](https://www.linkedin.com/in/nur-ameera-chan-240a9a242/),
[Mohammad Azri](https://www.linkedin.com/in/mohammadazri/), and
Afif Jazimin bin Saiful Zaidi.

## Proposed workflow

The team brief described a design using Llama 3, NLP, and Hugging Face sentiment,
emotion, and behaviour analysis. These were part of the hackathon proposal;
this archive does not contain model code or independent validation of those
integrations.

1. **Review the conversation.** The assistant examines buyer–seller messages
   for signals that may need further investigation.
2. **Request evidence.** The proposed flow accepts PDF bank statements or
   receipts as supporting proof.
3. **Check transaction fields.** The workflow compares the document's
   timestamp, amount, and recipient account with the transaction record.
4. **Route the outcome.** If the evidence matches, the proposal releases the
   held funds to the buyer. If it does not, the claim is monitored; repeated
   falsified claims would flag the account.
5. **Handle mismatched amounts.** For overpayment, the proposal asks the seller
   to return the excess amount within a set time and flags an ignored request.
   For underpayment, it asks the buyer for the remaining balance and escalates
   unresolved cases to a human.

These are **proposed product behaviours**, not verified production functions.
Any real payment release, fraud flag, or account action would require
implementation, controls, and review beyond the evidence available here.

## Design reflection

The workflow makes a useful distinction between conversational signals and
verifiable transaction evidence. The proposal uses AI to help triage the
conversation, while PDF proof and database checks determine the next route.
Its human escalation path matters when an amount mismatch remains unresolved.

## Evidence and media

| Material | What it shows |
| --- | --- |
| [Dispute-resolution workflow](media/dispute-workflow.png) | The team's proposed steps and outcome branches. |
| [ARLO chat screens](media/arlo-chat-screens.png) | Supplied interface screenshots of two conversations. |
| [Hackathon stage photo](media/hackathon-stage-faces-blurred.png) | Event setting and presentation screen. |
| [Team discussion photo](media/team-table-faces-blurred.png) | Candid group work at the event. |

**Privacy note:** All visible faces in the two public event photos were blurred
using an AI image-editing tool. These are privacy-edited versions of the supplied
photos, so non-face details may also differ from the originals. The original
unblurred photos are not published here. The workflow and chat screenshots were
provided as project materials and are displayed without modification.

## Thanks

Thank you to [Deriv](https://www.linkedin.com/company/derivdotcom/),
[JomHack](https://www.linkedin.com/company/jomhackmy/), and the mentors who
supported the hackathon and helped us refine the idea.
