# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [It is a game of higher lower, where the player must try an guess a random number from 1 to 100 withing 7 guesses, and is only told if their guess is too high or too low] Describe the game's purpose.
- [The hints were reversed, when a user inputted a higher number it would say go higher and when the inputted a lower number it would say go lower. The range of the hard difficulty was also wrong as it had a lower range than the normal difficulty ] Detail which bugs you found.
- [Claude generated the fix in logic_utils.py to correct the order of the hint messages and changed the hardcoded value for the hard difficulty to be higher than that of the normal difficulty] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. User enters guess of 50
2. Hint tells the user to Go HIGHER
3. User enters guess of 90
4. Hint tells the user to Go Lower
5. User enters the correct guess of 85 and wins the game

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```
============= test session starts ==============
platform darwin -- Python 3.13.15, pytest-9.1.1, pluggy-1.6.0
rootdir: /Users/eddy/Downloads/AIEngineering110/ai110-module1show-gameglitchinvestigator-starter
plugins: anyio-4.15.1
collected 4 items                              

tests/test_game_logic.py ....            [100%]

============== 4 passed in 0.01s ===============

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
