# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**
-You're allowed to enter numbers outside of the bounds of 1-100, expected out of bounds guesses to be rejected
-Doesn't take new guesses when the game is restarted, expected new guesses to be accepted and counted towards attempts taken
-Game over message still shows even after new game button is selected, expected message to go away once a new game was started

Document at least 3 bugs you found. Add rows as needed.

|        Input      |                Expected Behavior                 |      Actual Behavior      |                    Console Output / Error                       |
|Selected "New Game"|New Game begins and "Game Over" message disappears|"Game Over" message remains|"Game Over" message along with refreshed attempts remaining count|

|            Input              |                      Expected Behavior                     |                                    Actual Behavior                                        | Console Output/Error|
|Guess outside of bounds (1-100)| Doesn't take input since it's not between the bounds given | Hint is "Higher" if guess is greater than Answer and "Lower" if Guess is less than Answer |         none        |

|                Input                     | Expected Behavior |Actual Behavior|Console Output/Error|
|Guessed a number after starting a new game|Hint gives feedback|Nothing happens|        none        |
| | | | | 
| | | | |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
I used Gemini.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
It suggested I run python3 in my terminal commands instead of just python since the version I installed was python3. I verified the results by running the commands given in the problem statement and it worked. 
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
It suggested I keep the high/low logic as it was which was wrong. I ran the program knowing what the output should be and saw it didn't match

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I ran a test to see what the output was
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  I tested to see what the hint would say based on the guess. It showed the the agent successfully inverted the original logic so it would suggest the right direction instead of telling you about your current guess relative to the answer
- Did AI help you design or understand any tests? How?
It didn't only because I had a good understanding of how the tests would work for the errors I worked with

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
I learned that these states need to be updated in order for reruns to occur. Otherwise, you get stuck in the end-phase of a run without being able to exit. If explaining this to a friend, I'd say it's like scoring a goal in soccer but being unable to restart play at midfield by changing possession to the team that conceded the goal. 
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
I want to reuse the habit of checking the AI output for mistakes. Not doing so can be costly since it may not have all of the parameters it needs
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
I'd make my prompts more precise so it has less opportunity to misunderstand me. 
- In one or two sentences, describe how this project changed the way you think about AI generated code.
This project has made me more intentional about prompting AI with precise, direct specs that cover everything I need it to do. 
