# The challenge (Frontend Tech Lead)

As a Frontend Tech Lead candidate, your task is to provide a comprehensive solution proposal for the development of a real-time chat application. Your proposal should include a high-level architectural design, risk assessment, and a proof of concept to serve as a starting point for your development team.

Doodle is used by organizers to schedule meetings with participants: for this, the organizer can create meetings with an organizer frontend application. The participants can then vote on potential times of these meetings on a participation frontend application. Both frontends are static client-side applications and use a REST-based meeting service to collect the preferences of the participants.

We’d like to enable organizers and participants of each meeting to message each other in a chat component, which is integrated both on the organizer and the participation frontend applications.

In order to constrain this scenario further, we only want to support messages with text content and all users are authenticated. However we do want chat participants to see new messages without reloading the page. Although there are typically around 10 participants per meeting, the meeting service supports several 100’000s of meetings, with around 10’000 active users.

## What we expect

- Provide a concise document outlining your solution proposal, risk assessment, and architectural design.
- Include a link to the GitHub repository containing the proof of concept code.

> [!IMPORTANT]  
> The proof of concept does not need to have all the functionalities described in your solution proposal, but should illustrate and validate your architecture.

> [!NOTE]  
> Focus on the Frontend aspect in your solution. You are allowed to make certain assumptions about the Backend implementation and use mock servers in the proof of concept to showcase the functionality.

We understand your time is precious and would not want you to spend more than **4 to 6 hours** on this over the span of **one week** max. The outcome should be runnable locally on a UNIX-flavored OS (MacOS, Linux) in a common browser.

You can use Typescript, ideally with React. We want you to provide a responsive implementation. Keep in mind that Doodle is used worldwide and has to work on commonly used browsers.

We expect to hear back from you in **one week** from now, latest.

## Evaluation Criteria:

Your solution proposal will be evaluated based on the clarity of the architectural design, the thoroughness of risk assessment, and the viability of the proof of concept. Be prepared to discuss your decisions in detail during a follow-up interview, where you may also be asked to elaborate on specific aspects of your proposal.

## Next steps

Send an email with your solution and a link to your repository to `code-challenge@doodle.com`.

Make sure your email has the following subject: `FTL-<yourname>`. So for example, if your name were "Paul Smith",
your email subject would be `FTL-Paul Smith`

We will review your solution, we strive to get back to you in **1 week**. Sometimes it might take more.
