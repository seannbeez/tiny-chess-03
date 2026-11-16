# tiny-chess-03

A strong chess engine in 4 KB of Python for the make.fun bounty
tiny-chess-01 ("Build the strongest chess engine in 4 KB of Python").

`main.py` is the packed entrypoint (makefun compress of `engine.py`,
2,388 bytes). `engine.py` is the readable source (4,981 bytes).

Engine: 0x88 board, alpha-beta with PVS, transposition table with
mate-score adjustment, SEE-lite quiescence (cap 8), PeSTO-style tapered
king evaluation + bishop pair. 25,000 nodes/move, deterministic.

Local trial results (kit harness, LOCAL ESTIMATE — local Python 3.12.3
vs server 3.13): trial-0 Elo 1099, trial-1 Elo 708, trial-2 Elo 876,
mean 894. Below the 1,154 practice floor; not submitted.
