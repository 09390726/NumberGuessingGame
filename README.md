# NumberGuessingGame
You will design and implement a number guessing game where a player attempts to guess a randomly generated number between 1 and 100 within a limited number of attempts.

---

## Scope

### What the solution WILL do:
- Generate a random secret number between 1 and 100
- Accept player guesses via keyboard input
- Provide feedback after each guess (higher/lower)
- Track remaining number of guesses
- Display win or loss message with appropriate information
- Handle all guesses within a five-turn limit

### What the solution WILL NOT do:
- Allow unlimited guesses
- Accept guesses outside the 1-100 range
- Provide hints beyond higher/lower feedback
- Save high scores or game history
- Support multiple players or multiplayer modes
- Allow the player to restart without running the program again

---

## Functional Requirements

### FR1: Random Number Generation
**Input:** None (automated)  
**Process:** Generate a random integer between 1 and 100 (inclusive)  
**Output:** Secret number stored in program memory (not displayed to player)

### FR2: Accept Player Guess
**Input:** Integer value from player via keyboard  
**Process:** Store guess for comparison  
**Output:** None (data stored for processing)

### FR3: Compare Guess to Secret Number
**Input:** Player's guess, secret number, remaining guesses  
**Process:** 
- Compare guess to secret number
- Determine if higher, lower, or correct
- Decrement remaining guesses counter
**Output:** Feedback message ("HIGHER", "LOWER", or win message)

### FR4: Display Remaining Guesses
**Input:** Current count of remaining guesses  
**Process:** Calculate and format message  
**Output:** Display "[X] guesses left" after each turn

### FR5: Determine Game Outcome
**Input:** Guess comparison result, remaining guesses  
**Process:** 
- Check if guess is correct (player wins)
- Check if guesses remaining = 0 (player loses)
**Output:** 
- Win message: Appropriate congratulations
- Lose message: "You lose. The correct number is [X]."

---

## Non-Functional Requirements

### NFR1: Usability
- All prompts and messages must be clear and easy to understand
- The game flow must be intuitive for a first-time player
- Input prompts must clearly indicate the valid range (1-100)

### NFR2: Reliability
- The program must handle exactly five guess attempts
- The program must not crash if given invalid input
- The secret number must remain consistent throughout a single game

### NFR3: Maintainability
- Code must include comments explaining key sections
- Variable names must be descriptive (e.g., `secretNumber`, not `x`)
- Code must be properly indented following Python conventions

---

## Constraints

### Time Constraints
- **Total time available:** 100 minutes
- **Flowchart planning and approval:** ~25-30 minutes
- **Coding and testing:** ~60-65 minutes
- **Submission and cleanup:** ~5-10 minutes

### Technical Constraints
- **Language:** Python 3.x
- **Platform:** GitHub Classroom accessed via Codespaces
- **External libraries:** Only the `random` module may be imported
- **Development environment:** Web-based Codespaces editor

### Social/Usability Constraints
- Game must be playable by students with basic keyboard skills
- Messages must be appropriate for a school environment
- Instructions must be understandable by year-level peers

### Legal Constraints
- Must be your own original work
- Cannot copy code directly from AI assistants or online sources
- May reference Python documentation for syntax

---

## Starter Code Provided

```python
import random
secretNumber = random.randrange(1,100)
```

**Note:** You will need to add all remaining functionality to complete the game.

---

## Task Workflow

### STAGE 1: Planning (Must be completed FIRST)
1. Read this entire project brief carefully
2. On the printed flowchart template provided, draw the complete algorithmic flow of your program
3. Your flowchart must include:
   - Start and End symbols (oval)
   - Process steps (rectangles)
   - Decision points (diamonds)
   - Input/Output operations (parallelograms)
   - Flow arrows showing program direction
4. **Show your completed flowchart to your teacher for sign-off**
5. **You may NOT begin coding until your flowchart is approved**

### STAGE 2: Implementation
1. Once your flowchart is approved, access the GitHub Classroom assignment
2. Open the repository in Codespaces
3. Write your Python code following your flowchart
4. Test your program with multiple different scenarios
5. Ensure all functional requirements are met
6. Commit and push your final code to GitHub

---

## Expected Output Example

```
Enter your guess (1-100): 50
LOWER. 4 guesses left.
Enter your guess (1-100): 25
LOWER. 3 guesses left.
Enter your guess (1-100): 12
LOWER. 2 guesses left.
Enter your guess (1-100): 6
HIGHER. 1 guesses left.
Enter your guess (1-100): 9
LOWER. 0 guesses left.
You lose. The correct number is 8.
```

---

## Success Criteria

Your solution will be assessed on whether it:

**Scope & Requirements:**
- [ ] Generates a random number between 1-100
- [ ] Accepts player input for guesses
- [ ] Provides HIGHER/LOWER feedback accurately
- [ ] Tracks and displays remaining guesses correctly
- [ ] Limits player to exactly 5 attempts
- [ ] Displays appropriate win message when guess is correct
- [ ] Displays appropriate loss message with correct number when guesses run out

**Code Quality:**
- [ ] Flowchart accurately represents the final program logic
- [ ] Code is properly indented and formatted
- [ ] Variables have descriptive names
- [ ] Comments explain key sections of code
- [ ] Program runs without errors

**Submission:**
- [ ] Flowchart has teacher signature
- [ ] Code committed and pushed to GitHub Classroom
- [ ] Completed within the 100-minute time limit

---

## Tips for Success

1. **Plan thoroughly:** Your flowchart is your roadmap. A clear plan makes coding faster.
2. **Test frequently:** Run your program after adding each new feature.
3. **Use meaningful variable names:** `remainingGuesses` is better than `x`.
4. **Think about edge cases:** What happens on the first guess? The last guess?
5. **Manage your time:** Aim to have working code with 15 minutes remaining for testing and debugging.

---
