# The challenge (Principal Engineer)
Typically we have a frontend coding exercise at Doodle, in which the candidates implement a [chat application in Javascript](https://github.com/DoodleScheduling/hiring-challenges/tree/master/frontend-engineer/), with a provided design and a very simple polling API. However, for this leading position we want you to take it to the next level and focus on designing an architecture and communicating this architecture specification.

Doodle is used by _organizers_ to schedule _meetings_ with _participants_: for this, the organizer can create meetings with an organizer frontend. The participants can then vote on potential times of these meetings on a participation frontend. Both frontends are static client-side applications and use a REST based meeting service to collect the preferences of the participants.

We’d like to enable organizers and participants of each meeting to message each other in a chat component, which is integrated both on organizer and participation frontend. 

In order to constrain this scenario further, we only want to support messages with text content and all users are authenticated. However we do want chat participants to see new messages without reloading the page. Although there are typically only around 10 participants per meeting, the meeting service supports several 100’000s of meetings, with around 10’000 active users.

# What we expect

Please write a short specification for the messaging system, with the following aspects:

- Formalize requirements and quality goals
- Provide a high level system architecture diagram
- Provide a high level solution recommendation for a technical implementation
- Provide a high level overview of potential risks

We would then like for you to communicate this specification to potential relevant stakeholders in a 10-15 minute presentation, which serves as a starting point for a discussion.

We understand your time is precious and would not want you to spend more than 3 to 5 hours on this over the span of 1 week max.
