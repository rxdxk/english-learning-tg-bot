# English Learning Telegram Bot 🇬🇧

Async Telegram bot that helps users practise English: learning sessions, quizzes and a built-in translator,
with progress stored per user.

## Features
- Learning mode with word / phrase cards
- Tests with questions loaded at startup
- Translator command
- Multi-step flows built on aiogram FSM (states)
- Users and progress stored in SQLite
- Clean startup / shutdown hooks (DB open/close, table creation)

## Run
```bash
pip install aiogram environs
# .env
BOT_TOKEN=your_token
DB_FILE=bot.db
python main.py
```

## Structure
```
main.py              startup/shutdown hooks, polling
loader.py            Bot, Dispatcher, storage, DB
functions/
  handlers.py        commands & routing
  learn.py           learning mode
  tests.py           quizzes
  translator.py      translation
  states.py          FSM states
  keyboards.py       keyboards
db_api/              SQLite wrapper and users table
```

## Stack
Python · aiogram 3 (async) · FSM · SQLite · environs
