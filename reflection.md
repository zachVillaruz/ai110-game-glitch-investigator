# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- Game was very buggy. It sometimes said you had more attempts than you
actually did, would tell you that you needed to find a higher number when
you really needed a lower one (and vice versa), and the game was hard-coded
to give you a number from 1 to 100, even if the difficulties asked for
different bounds.

---

## 2. How did you use AI as a teammate?

- I used VSCode's CoPilot for this assignment.
- When fixing the hard-coded values, the AI said that the "issue is that the
"New Game" button hardcodes the range as 1-100 instead of using the current
difficulty setting." Their suggestion was to change it to low and high
variables instead, which I verified was what should've been done instead.
- When trying to fix the "Go HIGHER!" or "Go LOWER!" messages, the AI did
propose swapping the two messages around... However, they suggested swapping
them on Lines 46 and 47 too, the TypeError handler messages, causing the
messages to swap a second time, effectively bringing me back to where I was
initially with this problem.

---

## 3. Debugging and testing your fixes

- I decided a bug was really fixed when I re-ran the program and saw that it worked as intended. This meant playing with test cases, messing around with random numbers to see the result, and seeing if it passed the tests it was supposed to.
- I ran most of the tests manually, by playtesting and testing with random values. That was how I was able to find bugs like the swapped messages or the magic numbers from the code.
- Yes. Some bugs I didn't understand, like the TypeError message. It was only thanks to the AI explaining it to me that I was able to truly understand what was going on.

---

## 4. What did you learn about Streamlit and state?

- The secret number kept changing because the code to make a new secret number kept running each guess, when it should've only been run once when a new game session begins.
- Truth is, I don't really know how Streamlit works either, even after doing this project. So I don't think I could explain it to a friend that knows even less about it than me.
- The change I gave to allow the game to have a stable secret number was changing the update_score() function, removing the reassignment of the secret variable when it was run.

---

## 5. Looking ahead: your developer habits

- I think the next time I ask AI to help produce code, I think this project has taught me to be more mindful about how I prompt the AI, from giving more specific details and relevant information and making sure the AI has enough context to understand what I want.
- One thing I would do differently with AI next time is assess the code more before I am quick to turn to AI, as sometimes there are times where it is better to have human eyes looking at the code for an error, than an AI.
- I didn't really know how capable AI was when faced with a problem revolving around coding, so I was surprised to see it analyze the code and successfully understand what the issue was with it when I explained what I wanted.
