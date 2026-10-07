# AI Contribution Log – SLE-3 (Full C4 Model)

**Course:** 02AML204 – Introduction to Artificial Intelligence
**Name:** Sharvil S. Chavan | **PRN:** 25UAM085 | **Division:** B
**Date:** 03 October 2026

## AI Tool Used

- Claude (Anthropic)

## Summary

| Part of SLE-3 | What AI helped with | What I did myself |
| --- | --- | --- |
| System choice | – | Chose the Maze Solver (BFS / DFS) system from my SLE-1 and SLE-2 work |
| 1. Description | Drafted the wording from my SLE-1 and SLE-2 reports | Checked it matches my actual system and maze sizes |
| 2. Context diagram | Suggested the C4 structure; produced a first version | Reviewed it and confirmed actors and external dependencies (Python runtime, Matplotlib) |
| 3. Container diagram | Drafted the six containers and first diagram | Checked each container against `maze_search.py` |
| 4. Component diagram | Drafted components of the Search Engine and first diagram | Verified the flow (pop → goal test → expand → visited/parent → reconstruct) |
| 5. Code overview | Drafted the table of functions | Confirmed every function name and responsibility matches my code |
| 6. Design decisions | Helped phrase the points | Decided and can explain the reasoning myself |
| 7–8. AI note, conclusion | Drafted wording | Reviewed and edited so it reflects what I learned |

## Verification I Did

- [ ] Compared every container and function name with my SLE-2 code (`maze_search.py`)
- [ ] Checked that the diagrams match the system I actually built
- [ ] Checked the claims in the conclusion (BFS shortest path, node counts) against my SLE-2 results
- [ ] Made sure I can explain each level in my own words

> Tick the boxes only for what you really did.

## Prompts Used (examples)

Add 2–3 real prompts you gave to the AI here, for example:

1. "Help me structure a C4 model for my BFS/DFS maze solver."
2. _(your prompt)_
3. _(your prompt)_

## What I Learned

C4 showed me the same system at four levels of detail. I understood that BFS and DFS share almost everything and differ only in how the Frontier is handled (queue vs stack).

## Declaration

I used AI as a support tool for drafting and for first versions of the diagrams. I reviewed and understood the final design and can explain it.

**Signed:** Sharvil S. Chavan (25UAM085)
