# RUSH 01 - Indian Poker

| condition name | condition |
| :------------------ | ---------------- |
| File name to be submitted: | All necessary files |
| Available external modules: | All required modules |
| Note: | None |

Indian Poker is a psychological warfare game using trump cards. You need to implement a service that allows you to play this game online.

---

## Indian Poker Rules

It should be implemented based on the rules stated below.

### Game Ready
This game uses trump cards. Only 40 number cards are used in play, excluding jacks, queens, kings, and jokers from the trump cards.

One dealer and two players play cards and chips. In this subject, the server will act as a dealer, right?

### starting Game
Each player is dealt one face down card.

Place the received card on your forehead so that your opponent can see the card. Never look at your own cards.

Each player starts by betting 1 chip as a default.

### round
Now the game begins in earnest.

You can choose the number of chips to bet on each turn. What follows for each bet is as follows:

- **Same number as your opponent**: The round ends and the card is opened. The person with the highest number of cards wins.
- **Give up without betting**: If you give up, the other player unconditionally wins.
- **Bet more than your opponent**: The round continues.

You can bet with a minimum of 1 chip.

The winning player takes all bets.

If the same number is drawn when the card is opened, the next round is played while keeping the bet chips. (If there are no more cards, the bets are split between the chips.)

Do not return or add used cards to the card pack until the end of the game.

### game over

At the end of the round, if a player has no more chips or no more cards to deal, the game is over. The player with the most chips is the final winner.

> 💍 To learn more about this game, see [here] (https://en.wikipedia.org/wiki/Blind_man's_bluff_(poker)).

---

## Essential features to implement

### common
- Errors must be handled within the range that the user can move.
  - Handling errors also includes a developer predicting an error situation and notifying the user.

### user
- Supports external login / member registration process with OAuth function.
  - There must be at least one type, and the basic login (the procedure for logging in / registering by entering an email / password) does not have to be implemented.
- Each user must have a profile picture and nickname.
  - When logging in, the above two information must be displayed on the main page.
- When logging in to the service for the first time through OAuth, there should be a screen to receive user information.
  - Nickname must be more than n characters, and there must be no duplicates.
  - If the user does not designate a profile picture when signing up for membership, the profile picture should be designated as the default-image.

### game

#### starting Game
At the start of the game, you can create a new room or join an existing room.

##### Create room
- A user who creates a new room can become a host and set game conditions when creating a room.
  - The game conditions that the host can set when creating are as follows.
    - Turn time (recommended: between 10 and 30 seconds)
    - Number of chips per player (recommended: between 30 and 50)
- After the room is created, the host can check the code of the assigned room with four randomly given numbers.

##### Join the room
If you are joining a room that already exists, enter the code to join.

#### Game Progress
- All game information must be handled through socket communication.
- When the game starts, you should see a section where cards are shown and a dealing table session.
- If one player leaves during the game, the game is forcibly terminated.

> 💡 https://socket.io

##### card
- Your card and your opponent's card must be shown in the card section.
  - At this time, your card must be shown face down, and the opponent's card must be shown face up.
  - You must show your card at the end of the round.
  
##### Betting
- During a dealing table session, players must bet their chips.
  - You must show the currently hanging chip.
  - When placing a bet, you must show how much you are betting.
    - When placing a chip bet, it must be increased / decreased by one, and it must be communicated so that the other party can see it through the screen.
  - You must indicate the turn time available for betting.

---

## bonus

> 🔥 This item can only be evaluated if essential features are perfect.
- Everything can be executed with one command `docker-compose up -build`.
- You must be able to chat between two people.
  - In addition to chatting, system messages / game messages should be displayed together in the chat list.
    - System message: entry, exit (forced termination)
    - Game message: round start, bet, round result, game result
    - Chat / system messages / game messages should be displayed in different colors.
- 3 or more people must be able to participate in one game.
  - A feature must be implemented so that the host can set the maximum number of people when creating a room.
- You must use the WebRTC API to launch the video to the player's own and the opposing player's webcam.
- The service must be distributed so that it can be accessed not only locally but also in the external environment.