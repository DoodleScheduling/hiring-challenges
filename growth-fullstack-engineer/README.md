# The challenge (Growth Fullstack Engineer)

The Growth team at Doodle runs A/B tests. We show two versions of a page to different visitors and measure which one works better.

When users open their dashboard on doodle.com, they see a list of their polls. We want more people to create new polls. In this challenge you build a simple dashboard and test two versions of its "Create poll" button.

Please spend no more than **3 hours** on this. When you reach 3 hours, stop and write down what is left.

## What to build

### Backend

1. Load the polls from `assets/polls.json`. Add an endpoint that lists them, newest first. The title and the creation date are enough.
2. Give each visitor version A or version B of the button. Half of the visitors get A and half get B. A visitor always gets the same version.
3. Record two events: a visitor saw the button, and a visitor clicked the button.
4. Add an endpoint that shows the results for each version: how many visitors saw the button, how many clicked it, and the click rate.

### Frontend

1. Show the list of polls with the title and the date it was created.
2. Visitors do not log in. Each browser needs a visitor id that stays the same across reloads.
3. Show the version of the button the visitor is assigned to. Version A says "Create poll". You decide what version B changes.
4. A click on the button does not need to create a poll. It only needs to be recorded.

The design of the API is up to you. The page does not need to be pixel-perfect, but it must work on a phone and with a keyboard.

### Tests

Write tests for the backend. Cover at least the split and the results. Frontend tests are a plus.

### Questions

Answer these in your `README.md`. A few sentences each is enough.

1. What does version B change, and why do you think it will get more clicks?
2. How many visitors would you want before you trust the result? How did you get to that number?
3. The split should be close to 50/50. What could make it come out different, and how would you notice?
4. Is a click the right thing to measure? What else would you measure?

Also write in your `README.md` how to start the app and what you left out.

## Time

This is how we expect the 3 hours to be used. You can split them differently.

- Backend: 1 hour
- Frontend: 1 hour
- Tests: 30 minutes
- README and questions: 30 minutes

## Rules

- Backend: a JVM language, preferably Java. We use Spring Boot, and you can use any framework you like.
- Frontend: React with TypeScript. Doodle is used worldwide, so the page must work on commonly used browsers.
- Storage: keep everything in memory. You do not need a database.
- Running it: tell us how to start everything with one or two commands.
- AI tools: you can use them. Tell us which ones you used and for what. In the follow-up call we will ask you to walk us through your code and make a small change to it.

It is OK if you do not finish everything. Do what you think matters most first.

## What we look for

- The split works: about half of the visitors get each version, and a visitor always gets the same one.
- The numbers in the results are right.
- Clear answers to the questions.
- Readable code and useful tests.
- Small commits with useful messages.
- The page loads fast on a phone and is easy to use, also with a keyboard or a screen reader.

## Next steps

Keep your repository private. Add `kostiantyn-yemelianov-doodle` and `alexvan2` on GitHub as collaborators.

Send an email with a link to your repository to `code-challenge@doodle.com`.

Use the subject `GFS-<yourname>`. For example, if your name is "Paul Smith", the subject is `GFS-Paul Smith`.

We will review your solution and aim to reply within **1 week**. Sometimes it takes longer.
