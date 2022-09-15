# RUSH 00 - Create a Markdown based bulletin board

| | |
| --------------------:| ------------------ |
| Folder name to submit: | no limit |
| File name to be submitted: | no limit |
| Available external modules: | no limit |
| Note: | None |

### Condition

- Collaborate by creating API documents.
- UX/UI should be created with care. Wrong components should not be shown through state management.

### Default implementation

- On the main page, you can move to the next page through the navigation.
  - login
  - profile
  - Posts
- While data is being imported, the user should be able to know that the data is being imported.
  - Spinner, Skeleton
- For all errors/warnings/handling, it should be possible to recognize the status as a guide text.

#### Posts
- Posts should be displayed by rendering markdown in HTML.
- You can create/edit posts using the markdown editor.
  - Text of markdown syntax should be stored in DB.
- You can create/edit comments.
- Select and implement one of pagination and infinite scrolling.

> ℹ️
> react-simplemde-editor: https://github.com/RIP21/react-simplemde-editor
> tui.editor: https://github.com/nhn/tui.editor

#### login

- There should be a login/member registration page.
- You cannot access other pages without logging in.
- The separation of privileges according to the user privileges must be verified in both the frontend and the backend.
- Login should be maintained even if you use refresh / navigation.
- Implemented using jwt token.
  - Include only the necessary parts in the jwt token payload.
  - The expiry time of jwt token and cookie must be the same.
  - After the expiration time, a new jwt token is issued.

#### distribute

- Set ports for Frontend and Backend respectively as follows.
  - React: 4200 port
  - Express: 4242 port
- There must be .env_example in the submitted file.
 - Major information (PORT, API ENDPOINT, SECRET KEY) is managed through environment variables.

### bonus

- Everything can be executed with one command `docker-compose up -build`.
- Deploy using Heroku or cloud services.
- All items that can be implemented as a list must be implemented as either pagination or infinite scrolling.
- The admin page should exist separately, and the admin function in the basic implementation should be easily available inside the page.
  - You can block other users.
  - Posts/comments can be deleted.