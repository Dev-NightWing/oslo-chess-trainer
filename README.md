# ♟️ Oslo
### Interactive Discord Chess Puzzle Trainer

Oslo is a free Discord bot that transforms any server into an interactive chess puzzle training environment.

On most major chess platforms, puzzle training is restricted behind paywalls, limiting free users to only a few puzzles per day. As a result, many chess communities began manually sharing positions and solving puzzles together inside Discord channels — a process that relied on moderators to verify answers and often slowed puzzle solving.

Oslo solves this problem by bringing fast, collaborative chess training directly into Discord, allowing players to instantly launch puzzles and solve them interactively through chat using positions derived from a massive dataset of real games.

**Free & Open Source • Python Discord Bot • Chess Puzzle Trainer**

---

# 🚀 Features

♟️ Launch instant chess puzzles directly inside Discord  
🧠 Solve tactics through interactive back-and-forth gameplay  
🖼️ Automatically rendered chess boards for every puzzle  
📊 Skill-based difficulty tiers for players of all levels  
📚 Puzzles derived from real competitive chess games  
🏆 Track progress with personal puzzle statistics  
📈 Compete with friends through a server leaderboard  
👥 Multiple users can solve puzzles simultaneously  
⚡ Lightweight, efficient, and completely free to use  

---

# 🎯 Puzzle Difficulty Levels

Puzzles are grouped into rating pools so players of all strengths can train effectively.

| Difficulty | Rating Range |
|------------|--------------|
| Easy | 100 – 500 |
| Medium | 500 – 1000 |
| Hard | 1000 – 1500 |
| Insane | 1500 – 2000 |

Each difficulty pool is generated from filtered puzzle datasets to ensure appropriate tactical complexity for different player levels.

---

# 📚 Puzzle Source

All puzzles originate from the **Lichess Puzzle Database**, one of the largest publicly available collections of chess tactics.

Dataset source:  
https://database.lichess.org/

Custom preprocessing scripts were used to:

• decompress the original dataset  
• filter puzzles by rating ranges  
• extract puzzle themes and metadata  
• generate optimized puzzle pools for each difficulty tier  

The final puzzle pools are stored as lightweight JSON files used directly by the bot.

---

# ♟️ Example Puzzle Flow
!puzzle medium

Puzzle Rating: **1280**  
Theme: **fork, middlegame**

Opponent plays **Qe7**  
White to move.

Your move?

Users respond using chess notation:
-Nf3
-Qxd5
-O-O

The bot validates moves, updates the board, and continues the puzzle until the tactic is solved.

---

# 💬 Commands
This contains the commands that Oslo uses along with screenshots taken from real world interactions in a discord server.

## Start a Puzzle
!puzzle [easy | medium | hard | insane]

Launches a chess puzzle from the selected difficulty pool.


<img src="screenshots/puzzle_request.jpeg" width="300" />

---

## Reveal the Solution
!solution

Displays the correct tactical sequence for the puzzle if players wish to review the full line.

<img src="screenshots/solution.jpeg" width="300" />

---

## View Personal Puzzle Statistics
!profile

Displays a player's puzzle solving statistics including puzzles completed and success rate.

<img src="screenshots/profile.jpeg" width="300" />
---

## View Server Leaderboard
!leaderboard

Shows the top puzzle solvers within the server, encouraging friendly competition.

<img src="screenshots/leaderboard.jpeg" width="300" />

---

## Help and Guides
!guide
!notation

Commands that assist players with puzzle solving instructions and chess notation formatting.

Below is a visual example of **!guide** and **!notation** being used in real time on a server:

<table>
<tr>
<td><img src="screenshots/guide.jpeg" width="300"></td>
<td><img src="screenshots/notation.jpeg" width="300"></td>
</tr>
</table>

## Solving
Moves must be entered using a dash. (not case-sensitive)

Example:
-Nf3
-Qxd5

<img src="screenshots/solving.jpeg" width="300" />

---

# 📊 Early Community Interaction

Oslo was initially deployed in a small Discord chess community to observe real engagement.

**Before Oslo:** Only 10 puzzles had been manually shared by moderators over two months.
<img src="screenshots/before_oslo.JPG" width="300" />

**After Oslo:** Within the first **24 hours**, the community solved **over 200 puzzles** and generated **more than 1000 interactions**, making Oslo the **primary puzzle-solving tool** in the server.

Automation allowed players to launch puzzles instantly, solve them interactively, and track progress without relying on moderators.

Below is a visual proof of **after-Oslo activity**, shown side by side:

<table>
<tr>
<td><img src="screenshots/after_oslo_puzzle.JPG" width="300"></td>
<td><img src="screenshots/after_os!o_interactions.JPG" width="300"></td>
</tr>
</table>

---

# 💬 Community Feedback

Players particularly appreciated the ability to:

• launch puzzles instantly  
• track their puzzle progress  
• compete with friends on the leaderboard  

Community members began using the bot regularly instead of relying on manually shared puzzles.

<img src="screenshots/community_feedback1.jpeg" width="300" />

<img src="screenshots/community_feedback2.jpeg" width="300" />

<img src="screenshots/community_feedback3.jpeg" width="300" />

---

# 🛠️ Technology Stack

Oslo is built with a high-performance Python stack for real-time chess visualization:

• Core: Python & python-chess (Move validation / PGN parsing).

• Bot: discord.py (Asynchronous event handling).

• Graphics: CairoSVG, Pillow, and svglib (SVG-to-PNG board rendering).

• Data: zstandard (Efficient Lichess database decompression).


The architecture is fully asynchronous, supporting multiple simultaneous puzzle sessions across independent servers.

---

# 👤 Author

Made with ♟️ and ☕ by **Night Wing** (Alias)

Project Architect & Lead Developer

Oslo — Discord Chess Trainer is a community tool designed for tactical chess training. As an aspiring Computer Science student, I specialize in AI-assisted development—utilizing modern tools to architect, debug, and deploy scalable applications while maintaining digital privacy.
---

# 📜 License

This project is licensed under the **MIT License**.

