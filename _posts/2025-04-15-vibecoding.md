---
title: "Notes on vibecoding for reproducibility"
date: 2025-02-14
permalink: /weeknotes/2025/04/vibecoding/ 
---

## Notes on vibecoding as an RSE

(JW) At the end of last year I wrote about experimenting with Github CoPilot as an RSE - it had just been released free to all Github account holders. The research coding communities we work with are already getting a lot of use out of LLM-based coding assistants. Whether or not we enjoy or approve, it helps to prepare to review a lot of assisted code, and learn what to expect.

I tried out Cursor last week, spent an afternoon rapid prototyping a proof-of-concept for managing inventory of lab instruments and field sensors - something the organisation is gathering complex requirements for and looking for partnerships on. The "work" involved mostly watching it - first describing an application and an integration test suite, then setting it to auto-run, iteratively changing the requirements and data model then debugging the resulting test failures. Cursor did several weeks work while I watched, at a level of sophistication well beyond any coding assistant tools I've tried up to now. I burned up the credit in the "free tier" quite quickly, and even with a subscription you pay for top-ups.  

The experience of watching Cursor interact with itself did nudge me to reinstall CoPilot for VSCode and see what more I could get out of it as an RSE in a central team. A fairly typical part of the role is taking handover of code written by researchers who've since moved on to new projects, and the PIs need software professionals to ensure the code is reusable by others - testing, packaging, refactoring, creating environments. This can be a very mechanical process. I've been using this prompt in CoPilot:

_"Suggest a refactor of this script to ensure it runs from a main block, accepts path arguments with defaults rather than hardcoded paths. Write simple docstrings for new functions. Please don't delete any existing comments or documentation"_

We get incremental improvements. The code becomes more modular and testable, and better suited for running in a generic pipeline. These changes don't require much craft or care. With the best will in the world, it can be hard to prioritise taking [what EVERSE describe as "analysis code"](https://zenodo.org/records/10526785) to the level of "prototype tools", when research projects usually have many more goals than they have time to realise them in. This might have taken a few hours, rather than the short time it took both to do the work and write these notes.

I also tried this for another repository, with the prompt pasted in from a TODO list, for a more comprehensive refactor into an installable python package:

_"I'd like to make some improvements to this project -
Make it pip installable with pyproject.toml using setuptools, and turn the contents of `src` into a python package structure.
Load input data from s3
Pass data input as parameters, not hardcoded paths
Best faith attempt to create test cases with real samples
My data is in s3, not in the repo
"_

The prompt is explicit about pyproject/setuptools because the first suggestion was to introduce new dependencies on packaging tools that aren't part of python core. Every new complexity that we add makes it more likely that a researcher will run into blocks trying to reuse the code, and make it more likely to break in the future. Testing and documentation next, and we've mostly-automated away the mechanical work.

_Ok we need to add some very simple unit tests. We also need to create a virtual env, install the requirements and add the install instructions to the README. Please don't delete any of the existing documentation._

_What I would like are some simple github actions workflows that run the pytest tests, and a lint step, upload the coverage as an artifact, make sure to use non-deprecated upload actions._

I applied `black` and `flake8` for code formatting and lint testing myself - in the Cursor scenario it was doing that and making any necessary manual fixes. (Yes, we've tried switching to `ruff` but its insistence on argument and return value type hints feels like too much for research code).

I'm going back to read words I've shared in work chat recently: *"I would be so cautious about making recommendations for AI-assisted coding tools unless they are heavily qualified. There are so many concerns (business models, bias and inaccuracy, energy use, data worker exploitation, burdens on FOSS projects, the list is incomplete...) ... it feels like there's been a real shift in tone recently, from cynicism to anger, about the extent to which AI tooling is being imposed by big tech integrators whether we like it or not. Yes it's "democratising" but there are other ways to do that too, that don't involve skipping around an integrity minefield"*

Using "AI" as a peer programmer can be isolating. I'd rather collaborate directly with researchers or junior developers, share rules of thumb for basic code quality. Instead I'm both teaching CoPilot, and allowing myself to become a task-accepter. Yet the more one uses these tools, the harder it becomes to put them down. 

I don't offer an answer, other than this needs both consciousness-raising and culture change. My colleague Joe Marsh Rossney is proposing a workshop session at RSECon 2025 on writing a position statement for RSEs on the use of generative coding assistants. We're looking at the institutional guidelines for AI assisted code and how to bring them up to date. I'm always, though often not successfully, advocating for no-one to be coding alone on a project - for peer / mob development sessions with a social and knowledge sharing dimension to become the norm. Our central team is still new, and as such still picking up work towards the end of larger projects that have been running for some time. As we embed and grow, more input into the design stages of a project will help avoid the situation in which mechanical repair work needs to be done later on. Culture change is slow, and AI assistants of all kinds both embed existing assumptions about how business runs, and offer counter-incentives for changing the norms. Nothing is inevitable, and the second best time for critical examination is now. 



