# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

  a. The hints the game gave should've been the opposite
  b. The restart game doesn't actually work. There are no feedback of the game being restarted, so the 
     previous guess was still there and users can't input their new guesses.
  c. The difficulty levels dont reflect the actual difficulty, the easy had less attempts than the normal. And the range on the actual game does not reflect the difficulty.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| Guess: 40 | Hint: "Go Higher" | Hint: "Go Lower | Hint is misleading

| Pressing new game| Game restarts and everything resets | There is a new number but the user isn't able to guess and the guess history does not wipe for the new game | New Game button does not work

| Difficulty level set: easy| Attempted guess < attempted guess for medium and the game updates the directions correspondingly | Attempted guess > attempted guess for medium and the game does not update the directions.

|even and odd guesses| subtract points if it is incorrect| Add points if the guess is an incorrect even, and subtract if the guess is odd|  
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
    - claude

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
    - Claude said "If the guess is too high, the player needs to guess lower, and vice versa — so the message text is inverted. Same bug is duplicated in the fallback except TypeError branch below it. "

    And I think what claude recommended is what I had in mind, switching the hints around.

- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

 - I deleted some suggestions for additional features because it was deemed as bloat. 


---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?

  - if the behavior works as I intended, listed in the chart above.

- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.

  - I did the tests manually with clicks on the site

- Did AI help you design or understand any tests? How?
  AI gave me directions on how to test the updated fixes on the site.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  - Streamlit reruns stops the current execution and there are options to rerun the entire application or a function that is inputted. Sesstion state is when the application on the user side saves and updates the current state where the user is at.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.

    - Definitely find the bugs first before prompting and look through the individual functions that caused the bugs and prompt through the LLM and read through the analysis and changes that it proposes.

- What is one thing you would do differently next time you work with AI on a coding task?
  - Accepting the changes automatically.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  - Although in this project, it didn't release any confusing or suggested lots of uncessary code, I think its a good practice to read over and ask what each line it proposes does. 
