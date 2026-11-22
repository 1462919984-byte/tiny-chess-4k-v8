# tiny-chess-01 v8

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/1462919984-byte/tiny-chess-4k-v8/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/1462919984-byte/tiny-chess-4k-v8/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)


A 4 KB Python chess engine for the make.fun tiny-chess-01 competition.

- 0x88 mailbox board, negamax alpha-beta with iterative deepening
- fixed 120,000-node budget (deterministic; no clock)
- transposition table, history heuristic, LMR, null-move pruning
- quiescence search, check extension, pin detection
- material + piece-square evaluation
- an opening book keyed by Zobrist hash for the kit's practice openings

The engine talks to the env at `MAKEFUN_ENV_URL` (POST /game, /move).
`main.py` is the whole engine (an LZMA-packed payload), at most 4096 bytes.
