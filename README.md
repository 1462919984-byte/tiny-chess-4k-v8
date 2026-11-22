# tiny-chess-01 v8

A 4 KB Python chess engine for the make.fun tiny-chess-01 competition.

- 0x88 mailbox board, negamax alpha-beta with iterative deepening
- fixed 120,000-node budget (deterministic; no clock)
- transposition table, history heuristic, LMR, null-move pruning
- quiescence search, check extension, pin detection
- material + piece-square evaluation
- an opening book keyed by Zobrist hash for the kit's practice openings

The engine talks to the env at `MAKEFUN_ENV_URL` (POST /game, /move).
`main.py` is the whole engine (an LZMA-packed payload), at most 4096 bytes.
