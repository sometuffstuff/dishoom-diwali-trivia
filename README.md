# DISHOOM — Diwali Rapid Trivia
### by Balls By Picasso

A simple, offline-friendly browser trivia game designed for a game master and one player at a time.

## 1. What's included?

The application folder contains three main files:

```text
Dishoom-Trivia/
│
├── trivia_time.html
├── questions.txt
├── leaderboard.txt
└── README.md
```

- **trivia_time.html** — The actual trivia application.
- **questions.txt** — The editable question bank.
- **leaderboard.txt** — Stores player names, scores, optional phone numbers and dates.
- **README.md** — Instructions for running and maintaining the app.

## 2. Getting started

1. Keep all three application files in the same folder.
2. Open `trivia_time.html` using Google Chrome or Microsoft Edge.
3. On the application screen, find the **Offline Files** section.
4. Click **Load questions.txt** and select your questions file.
5. Click **Connect leaderboard.txt** and select your leaderboard file.
6. You're ready to play!

The application runs locally and does not require an internet connection or an online database.

**Browser compatibility:** Use a recent version of Chrome or Edge. These browsers support the file access features used by the application.

## 3. How to play

Each player gets a two-minute trivia round.

1. Click **Start Game**.
2. The countdown begins at 02:00.
3. The game master reads each question aloud.
4. The player answers verbally.
5. The game master marks the answer:
   - Correct: +1 point.
   - Wrong: 0 points.
   - Skip: Move to the next question without awarding a point.
6. The game advances automatically after a correct or wrong answer.
7. When time runs out, the round ends.
8. The player enters their name and may optionally provide their phone number.
9. Submit the score to add it to the leaderboard.

The game master can also undo the previous scoring action or end a round early.

## 4. Editing the questions

Open `questions.txt` using Notepad or any text editor.

Each question must occupy one line, using this format:

```text
Question | Correct answer
```

Example:

```text
What is the capital of Japan? | Tokyo
How many sides does a hexagon have? | Six
Which planet is known as the Red Planet? | Mars
```

Important rules:

- Questions are presented in the exact order in which they appear.
- The text before `|` is the question.
- The text after `|` is the answer.
- Blank lines are ignored.
- Lines beginning with `#` are comments and are ignored.
- Do not use `|` within the question itself.
- There is no fixed limit on the number of questions.

The correct answer is displayed on the game master's screen during gameplay.

After editing the question file, load it again in the application.

## 5. Leaderboard

The leaderboard is stored in `leaderboard.txt`.

Its format is:

```text
# DISHOOM LEADERBOARD
# Format: Name | Score | Phone | Date

Alex | 12 | 9876543210 | 2026-10-31T10:30:00.000Z
Priya | 10 |  | 2026-10-31T10:35:00.000Z
Rahul | 8 | 9123456780 | 2026-10-31T10:40:00.000Z
```

The fields are:

- **Name:** Player's name.
- **Score:** Total points earned.
- **Phone:** Optional phone number.
- **Date:** Submission timestamp.

Phone numbers are stored in the text file but are not displayed on the leaderboard.

The leaderboard is sorted by score, highest first. Players with equal scores are ordered alphabetically.

The application displays the top 10 entries.

### Leaderboard controls

- **Export CSV:** Downloads a spreadsheet-compatible copy of the leaderboard.
- **Reset Board:** Clears the leaderboard after confirmation.

The leaderboard file can also be edited manually using Notepad.

## 6. Data storage and backups

The application uses browser local storage as a backup and the connected text file as its persistent leaderboard file.

Important considerations:

- Scores are written to the connected text file when a player submits their score.
- The leaderboard is stored locally on the computer.
- No data is uploaded to an online server.
- Keep a backup copy of `leaderboard.txt` after events.
- If the browser's file permission expires, reconnect the leaderboard file using the application.
- Do not delete or replace the leaderboard file while the application is running.

## 7. Troubleshooting

**Questions aren't loading**

Check that:
- The file is named `questions.txt`.
- Every question follows the `Question | Answer` format.
- There are no malformed or empty question entries.
- You selected the correct file in the application.

**Leaderboard isn't saving**

Check that:
- You connected `leaderboard.txt`.
- Chrome or Edge has granted file access.
- The file has not been moved or deleted.
- You reconnect the file if the browser requests permission again.

**Leaderboard doesn't appear in the correct order**

Reconnect the leaderboard file and ensure score values are numeric.

**Application doesn't open**

Open `trivia_time.html` in a recent version of Chrome or Edge rather than opening it in a text editor.

## 8. Credits

**Event:** DISHOOM — Diwali Rapid Trivia  
**Created by:** Atul Hegde | Balls By Picasso

Enjoy the game. May the best trivia champion win!
