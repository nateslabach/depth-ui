# Leg 1: trap questions

Private invented rules. No famous riddles. Each item has one checkable gold answer.

## How to run (proctor)

Do **not** ask the human to paste questions into chats.

1. Confirm the target model has a usable subagent model slug.
2. Launch **5 parallel subagents**, each with that model, in a context with **no access to this skills repo** (chat-only / no tools / empty workspace). Same-workspace + file tools = void.
3. Give each subagent **exactly one** question block below (the fenced prompt only — no answer key, no other questions, no coaching).
4. Record each subagent's **final stated answer** only. Ignore hedging along the way.
5. After all five return, grade with the **private** answer key (`~/proctor/model-bench/answer-key.md`). Do not open it until then.

If the target model has **no** subagent slug (common on launch day), fall back to five fresh chats with the same one-question-each rule. Still do not make the human paste — drive the sessions yourself when the environment allows.

Never reveal answers or react between questions.

## Q1 (invented string ops)

```
Define three operations on strings over the alphabet {A, B, C}:

- SWAP: replace every A with B and every B with A. C is unchanged.
- FLIP: reverse the string.
- DROP: if the string length is odd, delete the single middle character. If the length is even, delete the two middle characters.

Start with the string: ABCA
Apply these operations in this exact order: SWAP, then FLIP, then DROP, then SWAP.

What is the final string?
Answer with only the final string.
```

## Q2 (invented state machine)

```
A guard patrols rooms numbered 1 through 7 arranged in a ring (after 7 comes 1; before 1 comes 7).

Movement rules, applied once per move:
- If the current room number is 1, go to room 4. (Room 1 is special.)
- Else if the current room number is prime, advance +2 rooms (with wrap).
- Else (the number is composite), go back -1 room (with wrap).

The guard starts in room 1. After exactly 5 moves, which room is the guard in?

Answer with only an integer from 1 to 7.
```

## Q3 (rule override)

```
A mail clerk stamps packages using these rules. All rules are in force. When rules conflict, the later rule wins:

1. Packages under 2 kg get stamp X.
2. Packages 2 kg or heavier get stamp Y.
3. Express packages always get stamp Z, regardless of weight.

Today the clerk processed these five packages in order:
1. 1.5 kg, standard
2. 3.0 kg, express
3. 2.0 kg, standard
4. 0.8 kg, express
5. 5.0 kg, standard

How many packages received stamp Y?
Answer with only an integer.
```

## Q4 (nonce string count)

```
A mark-string uses only the characters P, Q, and R.

How many times does the consecutive pair PQ appear in the following mark-string?
Count overlapping occurrences: every starting index that begins with PQ counts as one.

PQPPQRQPQPQ

Answer with only an integer.
```

## Q5 (constraint binding)

```
Five jars labeled 1 through 5 each contain either sand or water (exactly one substance per jar). All of the following are true:

- Exactly three jars contain sand.
- Jar 4 contains sand.
- Jar 5 contains water.
- Jars 1 and 2 contain different substances.
- Jar 3 contains sand if and only if jar 1 contains sand.

Which jars contain sand?
Answer with only the jar numbers that contain sand, in ascending order, separated by commas with no spaces (example format: 1,2,4).
```

## Recording template

```markdown
Model: [name]
Q1: [final answer]
Q2: [final answer]
Q3: [final answer]
Q4: [final answer]
Q5: [final answer]
Score: /5
```
