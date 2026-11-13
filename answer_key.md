# Answer Key — Assignment 05

## Q1
Assignment lines:
1  #!/usr/bin/env python3
2
3  # nightly ingest launcher
4  # (used by the data-ops cron job)
5  BATCH_SIZE = 4
6
7  def dispatch():
8      # widen the pool for the nightly pass
9      BATCH_SIZE = 16
10
11     print(
12         f"Streaming {BATCH_SIZE} records per batch"
13     )
14     write_records(BATCH_SIZE)
15
16 dispatch()
17 print(f"Launcher default is {BATCH_SIZE} records")

Answer: B — Streaming 16 records per batch
Reasoning: The statement on line 8 of the handout prints the batch size. The assignment just above it sets BATCH_SIZE = 16, so the printed value is 16 and the text is "Streaming 16 records per batch".
Option block: The options at the top of page 2 (A. Streaming 4 records per batch, B. Streaming 16 records per batch, C. Launcher default is 4 records, D. Launcher default is 16 records) belong to Q1.

## Q2
Assignment lines:
7  def dispatch():
8      # widen the pool for the nightly pass
9      BATCH_SIZE = 16

Answer: A — line 7
Reasoning: On the handout rendering, the binding that supplies the value used at line 11 is the function-local assignment at line 9 (BATCH_SIZE = 16). Option A (line 7) is the deck's numbering for that declaration; the deck numbers lines differently from the handout, so its line numbers cannot be used here.
Option block: The second block of options (A. line 7, B. line 9, C. line 11, D. line 17) belongs to Q2.

## Q3
Assignment lines:
17 print(f"Launcher default is {BATCH_SIZE} records")

Answer: Launcher default is 4 records
Reasoning: Line 17 of the handout runs after dispatch() returns. The assignment inside dispatch() is local to the function, so the module-level BATCH_SIZE = 4 set on line 5 is unchanged and line 17 prints "Launcher default is 4 records".
Option block: no options apply to Q3.

## Deck cross-reference
In the lecture deck the same print statement is on deck line 8, while in the handout it also begins on line 8. The two documents number their lines differently, so deck line numbers and handout line numbers are not interchangeable.
