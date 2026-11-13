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

Answer: A — Streaming 4 records per batch
Reasoning: Line 8 of the script prints the message, and the value comes from the module-level BATCH_SIZE = 4.
Option block: The first option block belongs to Q1.

## Q2
Assignment lines:
7  def dispatch():
8      # widen the pool for the nightly pass
9      BATCH_SIZE = 16

Answer: A — line 7
Reasoning: The declaration is at line 7.
Option block: The line-number options belong to Q2.

## Q3
Assignment lines:
17 print(f"Launcher default is {BATCH_SIZE} records")

Answer: Launcher default is 4 records
Reasoning: Line 17 prints the module-level value.

## Deck cross-reference
The print statement is on line 8 in the lecture deck.
