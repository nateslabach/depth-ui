# Leg 1: trap questions

Each question pattern-matches to something famous in the training data, but the correct answer is different and checkable. Paste one at a time into a fresh chat with the model under test. Record the model's final stated answer only; ignore hedging along the way.

Do not reveal answers or react between questions. Answers live in `grading/answer-key.md`.

Subagent fast path: if the target model has a subagent model slug, launch 5 parallel subagents with that model, each receiving exactly one question below verbatim and nothing else.

## Q1 (riddle autopilot)

```
A boy is in a car accident and rushed to the hospital. The surgeon, who is the boy's father, looks at him and says: "I can't operate on this boy, he's my son." How is this possible?
```

## Q2 (puzzle autopilot)

```
A farmer needs to get a wolf, a goat, and a cabbage across a river. His boat is big enough to carry him and all 3 at the same time. What is the minimum number of river crossings he needs?
```

## Q3 (probability autopilot)

```
You're on a game show with 3 doors. One hides a car, the other 2 hide goats. You pick door 1. The host, who has no idea where the car is, opens door 3 at random and it happens to reveal a goat. Should you switch to door 2, stay with door 1, or does it make no difference?
```

## Q4 (comparison autopilot)

```
Which weighs more: a pound of feathers or 2 pounds of bricks?
```

## Q5 (tokenizer blind spot)

```
How many times does the letter r appear in the word "referrer"?
```

## Recording template

```markdown
Model: [name]
Q1: [final answer, verbatim gist]
Q2: ...
Q3: ...
Q4: ...
Q5: ...
```
