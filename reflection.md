# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error | Location
|-------|-------------------|-----------------|------------------------|-----------|
|   40  | Go Higher             Go LOWER        none                      check_guess
|   50  | Go Lower              Go HIGHER       none                      check_guess
|  hard | increase range      decreases range   none                      get_range_for_difficulty

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
ChatGPT as a conversational and Claude
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
For the range of the hard difficulty, the AI suggested to change the range to 200 which is higher than the range of normal, which I think makes sense for an increased difficulty level
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.
Claude added quite a few test functions, some I though were unnecesary or repetetive, like a "test_comparison_is_numeric_not_lexicographic" method which pretty much does the same thing as a previously defined method so i decided to scrap it.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I tested it by rerunning the website
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
After fixing the bug that was causing the wrong hint to be displayed, I reran the script and checked manually by inputting numbers to make sure the output was correct
- Did AI help you design or understand any tests? How?
Yes, the comments it left for each test method made it clear what each one was testing and why.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
streamlit "reruns" literally reruns the script whenever something is changed, sort of like a rerendering, and session state keeps the state of a previous run that can be carried over to the rerun.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
Taking time to review the AI generated code as it can get out of hand, and also being more verbose with my prompts because I had to sort of prompt the same thing twice to get the desired result at times.
- What is one thing you would do differently next time you work with AI on a coding task?
Review the code and make sure I understand every line
- In one or two sentences, describe how this project changed the way you think about AI generated code.
This project didnt change my perspective on AI generated code too much, as I already know how much AI can hallucinate, but it made me see how much reviewing I really have to do.
