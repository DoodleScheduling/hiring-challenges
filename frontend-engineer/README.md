# The Challenge (Frontend Engineer)

We would like you to build a simple chat interface in TypeScript that sends and displays messages from all senders. The design should resemble the example below:

<img src="chat.png" width="400" alt="chat" />

The assets and additional documentation are available in the **assets** folder.

## Overview

Your task is to implement the frontend for a chat application. The backend API, which handles message storage and retrieval, has been shared as another repository.

**For the backend implementation details and setup instructions, please refer to the [Frontend Challenge Chat API repository](https://github.com/DoodleScheduling/frontend-challenge-chat-api)**.

### Frontend challenge Chat API Details

- **Authentication:** All message related endpoints require a Bearer token.
- **Endpoints:**
  - **GET /api/v1/messages:** Retrieves messages in reverse chronological order with optional pagination.
  - **POST /api/v1/messages:** Creates a new chat message.
- **Example cURL Commands after you run it locally:**

  **List all messages:**

  ```shell script
  curl http://localhost:3000/api/v1/messages \
    -H "Authorization: Bearer super-secret-doodle-token"
  ```

  **List 10 messages after a specific timestamp:**

  ```shell script
  curl "http://localhost:3000/api/v1/messages?after=2023-01-01T00:00:00.000Z&limit=10" \
    -H "Authorization: Bearer super-secret-doodle-token"
  ```

  **Send a message:**

  ```shell script
  curl -X POST http://localhost:3000/api/v1/messages \
    -H "Authorization: Bearer super-secret-doodle-token" \
    -H "Content-Type: application/json" \
    -d '{"message": "Hello world", "author": "John Doe"}'
  ```

## Challenge Requirements

- **Time Commitment:** Spend 4 to 6 hours on the challenge over the course of one week.
- **Technology:** Build the interface using React and TypeScript. Feel free to use frameworks like Next.js if desired.
- **Responsiveness:** The interface must be responsive and work smoothly on commonly used browsers and mobile devices.
- **Code Quality:** Maintain clear code readability, commit often with useful messages, and prioritize performance and accessibility.

## What We’re Looking For

- **Code Readability and Clean Architecture**
- **Commit Quality:** Frequent, descriptive commits.
- **Performance:** Fast load times and efficient rendering for mobile devices.
- **Accessibility:** User friendly design that is accessible to everyone.
- **Design Attention:** We are not looking for pixel perfect results, but we love attention to detail.

## Submission

Once completed, send an email with a link to your repository to `code-challenge@doodle.com` with the subject `FE-<yourname>`. For example, if your name is "Paul Smith", the subject should be `FE-Paul Smith`.

We will review your submission within one week although sometimes it might take a bit longer.

Good luck and happy coding!
