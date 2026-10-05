
Problems completed: #7, #8, #9, #11, #23

| Problem | Language | Files |
|---|---|---|
| 7 | ends with 10 | `n07.jff`, `n07t.txt`, `n07r.md` |
| 8 | starts with 01 and ends with 10 | `n08.jff`, `n08t.txt`, `n08r.md` |
| 9 | contains 10 | `n09.jff`, `n09t.txt`, `n09r.md` |
| 11 | 2nd-to-last bit is 1 | `n11.jff`, `n11t.txt`, `n11r.md` |
| 23 | odd length or s = 01 | `n23.jff`, `n23t.txt`, `n23r.md` |

Step-by-step computation screenshots: #8, #11, #23.

## Which problem(s) gave me the most trouble?
The problems I found hardest to understand were #8 and #23. In #8 the hard part was that one 1 has to count as both the end of the prefix 01 and the start of the suffix 10. In #23 the hard part was combining "odd length" with the single string 01 without breaking either one. I did not avoid any problem for being too hard, but I picked ones that follow the same guess-and-check pattern as #7. I used Chatgpt (an AI assistant) to explain how an NFA's guessing works, and to check my JFLAP screenshots against the expected results. I traced #7 by hand with its help to make sure I understood the method before building the others.

## Which problem(s) surprised me with a "gold-st-ring"?

In #23, the first design I was given used one start state that looped between odd and even and also had the 01 branch. That wrongly accepts 0101, because the loop returns to the start and the 01 branch can be taken again. Keeping the 01 branch off the loop fixed it. In #8, without the extra B to D edge on 1, 010 has no accepting thread. In future state-machine work, I'll write out the set of states after each symbol by hand first and check for any path that returns to a state with extra transitions.

## Other insights, comments, questions

Reaching an accepting state early doesn't count: a thread has to be in one when the input ends, as in 1101 in #11. Question: when does Step by State differ from Step with Closure in JFLAP?
