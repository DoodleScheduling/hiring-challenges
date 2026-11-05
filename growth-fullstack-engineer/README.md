# The challenge (Growth Fullstack Engineer)

The Growth team at Doodle runs A/B tests. We show two versions of a page to different visitors and measure which one works better.

Our goal is more paid subscriptions. When users open their dashboard on doodle.com, they see a list of their polls. In this challenge you build a simple version of that dashboard with an "Upgrade" button, and you test two versions of that button.

In a real product, the button would open a plans page where users pay. In this challenge there is no plans page and no payment. You measure clicks on the button instead.

Please spend no more than **3 hours** on this. When you reach 3 hours, stop and write down what is left.

## What to build

### Backend

1. Load the polls from `assets/polls.json`. Add an endpoint that lists all of them, newest first. Include the polls where `hidden` is true. The creation date is the `initiated` field, a Unix time in milliseconds. The title and the creation date are enough.
2. Give each visitor version A or version B of the button. Each new visitor has a 50% chance to get A and a 50% chance to get B. After that, the visitor always gets the same version. It is fine if this is lost when the server restarts.
3. Record two events: a visitor saw the button, and a visitor clicked the button. "Saw" means the page with the button has loaded.
4. Add an endpoint that returns the results for each version as JSON: how many visitors saw the button, how many of them clicked it, and the click rate. Count each visitor once, also when they reload the page or click more than once. The click rate is the number of visitors who clicked divided by the number of visitors who saw the button.

### Frontend

1. Show all polls with the title and the date it was created.
2. Visitors do not log in. Each browser needs a visitor id that stays the same across reloads. The browser or the server can create it.
3. Show the version of the button the visitor is assigned to. Version A says "Upgrade". Version B changes one thing. You decide what, for example the text, the place on the page or the look.
4. A click on the button does not need to open anything. It only needs to be recorded.

The design of the API is up to you. The page does not need to be pixel-perfect, but it must work on a phone and with a keyboard.

### Tests

Write tests for the backend. Cover at least the split and the results. Frontend tests are optional.

### Questions

Answer these in your `README.md`. A few sentences each is enough.

1. What does version B change, and why do you think it will get more clicks?
2. How many visitors would you want before you trust the result? How did you get to that number?
3. The split should be close to 50/50. What could make it come out different, and how would you notice?
4. A click on "Upgrade" is not a subscription. What would you measure to know whether version B brings more paid subscriptions?

Also write in your `README.md` how to start the app and what you left out.

## Time

This is how we expect the 3 hours to be used. You can split them differently.

- Project setup: 15 minutes
- Backend: 50 minutes
- Frontend: 55 minutes
- Tests: 30 minutes
- README and questions: 30 minutes

## Rules

- Backend: a JVM language, preferably Java. You can use any framework. We use Spring Boot.
- Frontend: React with TypeScript. Doodle is used worldwide, so the page must work on commonly used browsers.
- Storage: keep everything in memory. You do not need a database.
- Running it: tell us how to start it. One terminal for the backend and one for the frontend is fine.
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

Send an email with a link to your repository to `code-challenge@doodle.com`.

Use the subject `GFS-<yourname>`. For example, if your name is "Paul Smith", the subject is `GFS-Paul Smith`.

We will review your solution and aim to reply within **1 week**. Sometimes it takes longer.
