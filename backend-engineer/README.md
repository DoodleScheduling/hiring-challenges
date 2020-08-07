# The challenge (Backend Engineer)
When users go to their [dashboard](https://doodle.com/dashboard) on doodle.com, they will see a list of the doodles they have either created or
participated. Internally we call a doodle a _poll_.

We would like you to implement a simple Restful API with similar functionality. This is the functionality that your API
should support:

```
1. List all polls created by a user
2. Search polls by its title
3. List all polls created after a certain date
```

The design of the API is up to you.

In the **assets** folder you can find the `polls.json` file, which contain some data that you can use to bootstrap your 
database. We expect the responses from your API to be compatible with the shape of the polls in that file.

Your solution should be runnable locally using `docker-compose`. Don't forget to include all the dependencies of your 
service in the composer file, including your database system of choice. 

# Rules
We understand your time is precious and would not want you to spend more than **3 to 5 hours** on this over the span 
of **1 week** max. 

Please use a **JVM language**, preferably Java. Feel free to use any framework, like Spring for example.

# What we expect
It is OK if the challenge is not completed. Try to **prioritize** it by what you think is more important. Please include
a `README.md` file, that describes to us what motivated your technology choices, how you tackled the task, what you 
would do differently were you given more time, what you would differently a second time around, etc.

Here are some pointers for you of things we will be looking for:

* Commit often, write useful commit messages
* Design, we do like attention to detail
* Code readability
* Performance 

# Next steps
Send an email with a link to your repository solution to `code-challenge@doodle.com`.

Make sure your email has the following subject: `BE-<yourname>`. So for example, if your name were "Paul Smith", 
your email subject would be `BE-Paul Smith`

We will review your solution, we strive to get back to you in **48 hours**. Sometimes it might take more.
