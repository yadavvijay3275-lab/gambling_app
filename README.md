# gambling_app
# 🎰 THE FELT TABLE

### *A Virtual Casino-Style Gaming Experience*

**Product Requirements Document — Version 1.0**

> **Project Type:** College / Educational Project
> **Platform:** Web Application
> **Credits:** Virtual Demo Credits Only
> **Status:** Version 1 — MVP

---

# 01 — THE IDEA

## What is The Felt Table?

**The Felt Table** is an interactive casino-style web application where users can experience simple luck-based games using **virtual credits**.

The goal is not real-money gambling.

The goal is to create a realistic-looking, interactive gaming experience while learning how a modern full-stack web application works.

The application combines:

🎨 Attractive UI
🎮 Interactive Games
💰 Virtual Credit System
🔐 User Authentication
📊 Game History
⚡ Real-time Balance Updates
🗄️ MySQL Database
☕ Spring Boot Backend

---

# 02 — THE EXPERIENCE

The user should feel like they are entering a small virtual gaming lounge.

### Experience Flow

```text
          ENTER
            ↓
       🔐 LOGIN
            ↓
      💰 GET CREDITS
            ↓
      🎮 CHOOSE GAME
            ↓
       🎲 PLAY
            ↓
    ┌───────┴───────┐
    ↓               ↓
   WIN             LOSE
    ↓               ↓
💰 REWARD       💸 DEDUCT
    └───────┬───────┘
            ↓
       📜 HISTORY
```

The experience should be:

**Simple → Fast → Interactive → Visual → Easy to understand**

---

# 03 — PRODUCT VISION

> **"Make a casino-style gaming experience simple enough for anyone to understand and interesting enough to keep exploring."**

The application should not feel like a boring CRUD college project.

Instead, it should feel like a small gaming product.

---

# 04 — TARGET USER

### Primary User

College students and users who want to experience a simple browser-based gaming application using virtual credits.

### Example User

**Rahul, 20**

He opens the application.

```text
Welcome Rahul 👋

Your Balance
50,000 Credits

Choose Your Game

🎰 Slots
🔢 Guess
🥤 Three Cups
```

He chooses a game, places a virtual-credit bet, plays, and immediately sees the result.

---

# 05 — CORE FEATURES

## 🎮 1. Game Lobby

The home screen is the main gaming lobby.

It contains:

```text
┌─────────────────────────────────┐
│       THE FELT TABLE            │
│                                 │
│   💰 50,000 CREDITS             │
│                                 │
│  ┌────────┐ ┌────────┐ ┌──────┐ │
│  │ 🎰     │ │ 🔢     │ │ 🥤   │ │
│  │ SLOTS  │ │ GUESS  │ │ CUPS │ │
│  └────────┘ └────────┘ └──────┘ │
│                                 │
│          VIEW HISTORY            │
└─────────────────────────────────┘
```

---

# 06 — GAME 01

# 🎰 SLOT MACHINE

### Concept

A simple three-reel slot machine.

The player selects a virtual-credit bet and presses **SPIN**.

Example:

```text
┌───────────────────────┐
│      SLOT MACHINE     │
│                       │
│   🍒  |  ⭐  |  🍒    │
│                       │
│       YOU WIN!        │
│                       │
│   Bet: 1,000          │
│   Reward: 2,000       │
│                       │
│       [ SPIN ]        │
└───────────────────────┘
```

### Requirements

* Minimum bet: 1,000 credits
* Three generated symbols
* Backend generates the result
* Backend calculates reward
* Balance updates automatically
* Result saved to history

### Possible symbols

```text
🍒 Cherry
🍋 Lemon
🔔 Bell
⭐ Star
💎 Diamond
7️⃣ Seven
```

---

# 07 — GAME 02

# 🔢 GUESS THE NUMBER

### Concept

The system secretly generates a number.

The player tries to guess it.

Example:

```text
I'm thinking of a number...

1 ───────── 10

Your Guess:
[ 7 ]

Bet:
[ 1,000 ]

       [ GUESS ]
```

Result:

```text
🎉 CORRECT!

You guessed the number.

Reward: 2,000 Credits
```

### Requirements

* Backend generates random number
* User submits a guess
* Backend checks result
* Balance updates
* Result saved in history

---

# 08 — GAME 03

# 🥤 THREE CUPS

### Concept

Three cups are displayed.

One cup secretly contains the winning position.

```text
       🥤      🥤      🥤
        1       2       3

              ↓

       PICK ONE
```

User chooses one.

The backend randomly selects the winning cup.

Example:

```text
Your Cup: 2
Winning Cup: 2

🎉 YOU FOUND IT!

Reward: 2,000 Credits
```

---

# 09 — VIRTUAL CREDIT SYSTEM

The entire application uses **virtual credits**.

### Starting Balance

```text
50,000 Credits
```

Example:

```text
Starting Balance      50,000
       ↓
Bet                   -1,000
       ↓
Win Reward            +2,000
       ↓
New Balance           51,000
```

### Important Rule

The frontend never directly changes the balance.

Only the backend can:

* Deduct credits
* Add rewards
* Save transactions
* Return updated balance

---

# 10 — USER ACCOUNT

Users can create their own account.

### Registration

```text
Full Name
Email
Username
Password

[ CREATE ACCOUNT ]
```

### Login

```text
Username
Password

[ ENTER TABLE ]
```

After login:

```text
Welcome back, Rahul 👋
```

---

# 11 — GAME HISTORY

Every game creates a history record.

Example:

| Game     |   Bet | Result | Reward |
| -------- | ----: | ------ | -----: |
| 🎰 Slots | 1,000 | WIN    |  2,000 |
| 🔢 Guess | 1,000 | LOSS   |      0 |
| 🥤 Cups  | 2,000 | WIN    |  4,000 |

The history page gives the user a complete view of their previous games.

---

# 12 — DASHBOARD

The dashboard should answer four questions immediately:

### 💰 How many credits do I have?

### 🎮 What games can I play?

### 📜 What did I play recently?

### 📊 How am I performing?

Example:

```text
╔══════════════════════════════════╗
║       WELCOME TO THE TABLE       ║
╠══════════════════════════════════╣
║                                  ║
║       YOUR BALANCE               ║
║       48,500 CREDITS             ║
║                                  ║
╠══════════╦══════════╦════════════╣
║ 🎰       ║ 🔢       ║ 🥤         ║
║ SLOTS    ║ GUESS    ║ THREE CUPS ║
╚══════════╩══════════╩════════════╝
```

---

# 13 — USER JOURNEY

## First Visit

```text
Landing Page
     ↓
Create Account
     ↓
50,000 Credits
     ↓
Game Lobby
```

## Returning User

```text
Login
 ↓
Dashboard
 ↓
Continue Playing
```

---

# 14 — APPLICATION PAGES

### Page 1 — Landing / Login

Purpose:

Introduce the application and authenticate the user.

---

### Page 2 — Register

Purpose:

Create account.

---

### Page 3 — Game Lobby

Purpose:

Show available games and balance.

---

### Page 4 — Slot Machine

Purpose:

Play slot game.

---

### Page 5 — Guess the Number

Purpose:

Play number game.

---

### Page 6 — Three Cups

Purpose:

Play cup game.

---

### Page 7 — History

Purpose:

View previous games.

---

# 15 — DATABASE DESIGN

## Users

```text
users
────────────────────────
id
full_name
email
username
password
balance
created_at
```

## Game History

```text
game_history
────────────────────────
id
user_id
game_name
bet_amount
result
reward
created_at
```

### Relationship

```text
             USER
              │
              │
        ┌─────┴─────┐
        ↓           ↓
     GAME 1       GAME 2
        ↓           ↓
     GAME 3       GAME 4
```

One user can have many game-history records.

---

# 16 — TECHNICAL ARCHITECTURE

```text
┌─────────────────────────────┐
│        FRONTEND             │
│                             │
│ HTML + CSS + JavaScript     │
└──────────────┬──────────────┘
               │
             REST API
               │
┌──────────────▼──────────────┐
│        SPRING BOOT          │
│                             │
│ Controllers                 │
│       ↓                     │
│ Services                    │
│       ↓                     │
│ Repositories                │
└──────────────┬──────────────┘
               │
┌──────────────▼──────────────┐
│           MYSQL             │
│                             │
│ Users + Game History        │
└─────────────────────────────┘
```

---

# 17 — TECHNOLOGY STACK

| Layer           | Technology      |
| --------------- | --------------- |
| Frontend        | HTML            |
| Styling         | CSS             |
| Interaction     | JavaScript      |
| Backend         | Java            |
| Framework       | Spring Boot     |
| API             | REST            |
| Database        | MySQL           |
| ORM             | Spring Data JPA |
| Build           | Maven           |
| IDE             | VS Code         |
| Version Control | Git + GitHub    |

---

# 18 — API DESIGN

## Authentication

```text
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
GET  /api/auth/me
```

## User

```text
GET /api/user/balance
```

## Games

```text
POST /api/games/slot
POST /api/games/guess-number
POST /api/games/three-cups
```

## History

```text
GET /api/history
GET /api/history/{id}
```

---

# 19 — API FLOW

Example: Slot Machine

```text
User clicks SPIN
       ↓
Frontend sends bet
       ↓
POST /api/games/slot
       ↓
Spring Boot
       ↓
Check Login
       ↓
Check Balance
       ↓
Generate Result
       ↓
Calculate Reward
       ↓
Update Balance
       ↓
Save History
       ↓
Return Result
       ↓
Frontend updates screen
```

---

# 20 — SECURITY MODEL

Security principle:

> **Never trust the browser with important game logic.**

The frontend can request:

```text
"Play Slot with 1,000 credits"
```

But the frontend cannot say:

```text
"I won 50,000 credits."
```

The backend decides everything.

### Backend controls:

✔ Random result
✔ Win/Loss
✔ Reward
✔ Balance
✔ Game history
✔ User authentication

---

# 21 — VALIDATION

The system must prevent:

### Invalid Bet

```text
0
-500
empty
```

### Insufficient Balance

```text
Balance = 500

Bet = 1,000

→ Not allowed
```

### Invalid Game Input

Example:

```text
Guess = 100

Allowed = 1–10

→ Invalid
```

---

# 22 — ERROR EXPERIENCE

Errors should not look like technical server messages.

Instead of:

```text
HTTP 400 Bad Request
```

Show:

```text
⚠️ Invalid bet amount.

Please enter a valid virtual-credit amount.
```

---

# 23 — UI/UX DESIGN DIRECTION

## Visual Style

The application should have a:

**Premium Gaming Lounge** feel.

### Design principles

* Dark interface
* High contrast
* Large buttons
* Clear balance
* Game cards
* Smooth transitions
* Minimal clutter
* Mobile responsive

### Avoid

❌ Too many colors
❌ Too many animations
❌ Complicated menus
❌ Tiny buttons
❌ Unnecessary features

---

# 24 — INTERACTION DETAILS

When the user clicks **SPIN**:

```text
READY
 ↓
SPINNING...
 ↓
SYMBOLS REVEAL
 ↓
RESULT
 ↓
BALANCE UPDATE
```

When the user wins:

```text
🎉
YOU WON!

+2,000 Credits
```

When the user loses:

```text
Better luck next time.

-1,000 Credits
```

---

# 25 — RESPONSIVE DESIGN

The application must work on:

```text
Desktop
Laptop
Tablet
Mobile
```

Example mobile layout:

```text
┌─────────────────┐
│ THE FELT TABLE  │
│                 │
│ 50,000 CREDITS  │
│                 │
│ 🎰 SLOTS        │
│                 │
│ 🔢 GUESS        │
│                 │
│ 🥤 THREE CUPS   │
│                 │
│ 📜 HISTORY      │
└─────────────────┘
```

---

# 26 — PROJECT STRUCTURE

```text
the-felt-table/
│
├── README.md
├── PRD.md
├── .gitignore
├── pom.xml
│
├── docs/
│   └── screenshots/
│
└── src/
    └── main/
        ├── java/com/gamble/
        │
        │   ├── GambleWebApplication.java
        │   │
        │   ├── controller/
        │   │   ├── AuthController.java
        │   │   ├── GameController.java
        │   │   └── HistoryController.java
        │   │
        │   ├── service/
        │   │   ├── AuthService.java
        │   │   ├── GameService.java
        │   │   └── HistoryService.java
        │   │
        │   ├── repository/
        │   │   ├── UserRepository.java
        │   │   └── GameHistoryRepository.java
        │   │
        │   ├── model/
        │   │   ├── User.java
        │   │   └── GameHistory.java
        │   │
        │   └── dto/
        │       ├── LoginRequest.java
        │       ├── RegisterRequest.java
        │       └── GameRequest.java
        │
        └── resources/
            ├── application.properties
            │
            └── static/
                ├── index.html
                ├── login.html
                ├── register.html
                ├── games.html
                ├── history.html
                │
                ├── css/
                │   └── style.css
                │
                └── js/
                    ├── auth.js
                    ├── app.js
                    ├── games.js
                    └── history.js
```

---

# 27 — DEVELOPMENT ROADMAP

## Phase 1 — Foundation

```text
Spring Boot
MySQL
JPA
Project structure
```

## Phase 2 — Authentication

```text
Register
Login
Logout
Session
```

## Phase 3 — Virtual Economy

```text
Starting credits
Balance
Balance validation
```

## Phase 4 — Games

```text
Slot Machine
Guess the Number
Three Cups
```

## Phase 5 — History

```text
Save games
Display history
```

## Phase 6 — Frontend

```text
Dashboard
Game screens
Animations
Responsive design
```

## Phase 7 — Security

```text
Session validation
Input validation
Authorization
```

## Phase 8 — Final

```text
Testing
Documentation
GitHub
Screenshots
Demo
```

---

# 28 — MVP PRIORITY

### 🔴 Must Have

* Register
* Login
* Virtual balance
* Slot Machine
* Guess the Number
* Three Cups
* Game history
* MySQL
* Spring Boot
* Responsive frontend

### 🟡 Nice to Have

* Animations
* Sound effects
* Statistics
* Leaderboard
* Dark/light theme

### 🟢 Future

* Achievements
* Admin analytics
* More virtual games
* Advanced game statistics

---

# 29 — TESTING CHECKLIST

## Authentication

* [ ] Register
* [ ] Login
* [ ] Logout
* [ ] Wrong password
* [ ] Duplicate username

## Balance

* [ ] Starting credits
* [ ] Winning updates balance
* [ ] Losing updates balance
* [ ] Insufficient balance blocked

## Games

* [ ] Slot works
* [ ] Guess works
* [ ] Three Cups works

## History

* [ ] Game saved
* [ ] History displayed
* [ ] Correct user history only

## Security

* [ ] Login required
* [ ] User isolation
* [ ] Backend controls balance
* [ ] Backend controls results

## UI

* [ ] Desktop
* [ ] Tablet
* [ ] Mobile
* [ ] Error messages
* [ ] Loading state

---

# 30 — SUCCESS CRITERIA

The project is successful when a new user can:

```text
Register
   ↓
Login
   ↓
Receive 50,000 Credits
   ↓
Choose a Game
   ↓
Place Virtual Bet
   ↓
Play
   ↓
See Result
   ↓
See Updated Balance
   ↓
Check History
```

without needing any explanation.

---

# 31 — COLLEGE PROJECT VALUE

This project demonstrates knowledge of:

### Frontend

* HTML
* CSS
* JavaScript
* DOM
* Fetch API
* Responsive design

### Backend

* Java
* Spring Boot
* REST API
* Controllers
* Services
* Repositories

### Database

* MySQL
* SQL
* Relationships
* JPA/Hibernate

### Software Engineering

* Authentication
* Validation
* Session management
* Error handling
* Git/GitHub
* Project documentation

---

# 32 — PROJECT IDENTITY

## Name

**The Felt Table**

## Tagline

> **"Your Game. Your Luck. Your Table."**

## Alternative Taglines

> **"Step In. Pick a Game. Test Your Luck."**

> **"A Virtual Gaming Experience, Built for the Web."**

---

# 33 — IMPORTANT DISCLAIMER

**The Felt Table is an educational/college project using virtual demo credits only.**

It does not support:

* Real-money betting
* Deposits
* Withdrawals
* UPI payments
* Payment gateways
* Cash prizes
* Financial transactions

The credits displayed in the application have no real-world monetary value.

---

# 34 — DEFINITION OF DONE

The project is complete when:

✅ User registration works
✅ Login works
✅ Session authentication works
✅ 50,000 virtual credits are assigned
✅ Slot Machine works
✅ Guess the Number works
✅ Three Cups works
✅ Balance updates correctly
✅ Game history is saved
✅ Dashboard works
✅ Frontend is responsive
✅ Backend controls game results
✅ Users cannot access other users' data
✅ MySQL works
✅ README exists
✅ PRD exists
✅ GitHub repository is ready

---

# FINAL PRODUCT

```text
                 🎰
          ┌──────────────┐
          │ THE FELT     │
          │    TABLE     │
          └──────┬───────┘
                 │
        ┌────────┴────────┐
        │                 │
       🎰                🔢
     SLOTS              GUESS
        │                 │
        └────────┬────────┘
                 │
                🥤
             THREE CUPS
                 │
                 ↓
          💰 VIRTUAL CREDITS
                 │
                 ↓
            📜 HISTORY
```

**The goal is simple:**

### Build a project that looks like a game, but teaches real full-stack development.
