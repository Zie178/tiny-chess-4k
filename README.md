# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Zie178/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Zie178/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python (main.py is 3,465 bytes, packed with the make.fun compress tool from the readable source in engine.py). It plays through the make.fun environment protocol: a 0x88 board, negamax alpha-beta search with PVS, quiescence over captures, promotions and check replies, an exact-only transposition table, MVV-LVA ordering, incremental material + piece-square evaluation with Zobrist hashing, and full repetition handling — it replays the game history and scores repeated positions inside the search, so it avoids giving away draws when it stands better and steers for them when it stands worse. Deterministic: a fixed, phase-aware node budget per move, never a clock.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

Point MAKEFUN_ENV_URL at a make.fun environment server (see the tiny-chess-01 kit); the engine polls it for games and answers with UCI moves.

---

<sub>Entered on [make.fun](https://make.fun/?ref=bejbkp9b&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
