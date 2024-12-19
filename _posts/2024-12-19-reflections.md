---
title: "Random reflections at the end of 2024"
date: 2024-12-19
permalink: /weeknotes/2024/12/reflections/ 
---

## Random reflections at the end of 2024

(JW) Perhaps this section of the site should be "monthnotes" rather than weeknotes - a week flashes by, especially when working part-time hours and especially at this time of year!

Colleagues are starting to drift off for the holidays, which in Scotland last for us until Jan 6th. This always feels like a good time to do a small amount of investigative, exploratory work.

A project that more of us will be engaged with next year is the [Floods and Droughts Research Infrastructure](https://fdri.org.uk/). UKCEH maintains a network of long-term monitoring stations called [COSMOS-UK](https://cosmos.ceh.ac.uk/) which use cosmic rays to do soil moisture measurement - the "cosmic" makes it sound so sci-fi! Each of the COSMOS-UK sensors captures an image five times a day - a fish-eye perspective with two hemispheres. It's meant to help assess the state of the site, animal incursion etc, but also offers monitoring of seasonal conditions, and there's a continuous record of images stretching back for ten years. I just saw my first sample of it today; it's a fascinating collection full of unexpected potential.

We're hoping to draw on the more experimental work on image [machine learning pipelines for plankton microscope imagery](https://github.com/NERC-CEH/plankton_ml) when we work on this project; it will be a cloud-based deployment with very different infrastructure expectations, and more engagement from the development team in Environmental Data Science.

In the meantime, it's nice to have the opportunity to explore the data with an eye to what we can get out of it with off-the-shelf deep learning models. I made the tactical error of starting this in a Google Colab notebook, for quick and easy access to a GPU. It was an opportunity to experience the insistent integration with Google Gemini that Colab now provides by default. This came on top of an hour spent exploring all the VSCode integration with the new free, enabled-by-default version of Github CoPilot.

Personally I've got mixed feelings and mixed experiences with AI-assisted coding - the environmental and social impact of building and running large language models, the volume of free training data that interacting with them provides the few very large tech companies integrating them into seemingly everything, as well as their frequent error-proneness. But one has to recognise that for researchers who develop software on the side, and whose desired outcomes are better analysis and well-received publications, these tools are going to feel useful. As RSEs we have to know and experience their pain points, provide guidance around precaution for data harvesting in the default settings, and attempt to see the potential as reproducibility support tools (creating test suites and CI pipelines, offering refactoring feedback, seeding documentation).

But the experience of spending a couple of hours with AI-assisted coding tools has driven me to writing! Speaking as a human, I hope to display an essential kindness and cheerful ignorance when working with others on co-developing software. I hope our [team agreement](https://github.com/ukceh-rse/team-agreement) reflects that. The prompts and models behind CoPilot and Gemini don't seem to leave much space for uncertainty, humility or comedy. I'm left with quite a lot to reflect on about how a practise of "social coding" will look, filtered through robot eyes...

A recent bright spot for me has been the receipt of a Software Sustainability Institute Fellowship for 2025. It's a really different angle for me personally, not engaging with software directly at all, but in trying to help bring about a culture of reproducible open _hardware_ for environmental monitoring research. I'm hoping to bring field researchers and instrument engineers together with electronics hobbyists for a series of hands-on, very interactive workshops, and create and document a model for running more. There's a lot of prior art out there already, both for [open science hardware community organising](https://openhardware.science/) as well as low-cost, low-power sensors for unexpected applications.

The folks at Forest Research invited our Edinburgh office to a screening of a recording of a ["verbatim play" made from interviews with forestry researchers](https://hollywoodforest.com/2024/06/06/three-words-for-forest-exploring-uncertainty-in-a-time-of-climate-crises-the-new-leaves-network-arising-in-scotland/). I left that screening quietly simmering with thoughts, from what bioacoustic sensors could tell us about future forest health conditions, to how the models of partial, slow regeneration of homogenous industrial forest could eventually apply to regenerating technology infrastructure dominated by a few large monocultures. None of which thoughts I've even made time to process; but while writing this I've stumbled across a fascinating review article on [150+ years of bark beetle bioacoustics](https://resjournals.onlinelibrary.wiley.com/doi/full/10.1111/phen.12453). I feel lucky to have a few quiet days to let ideas simmer, before the main-event project work resumes in the New Year.

I hope we're all looking forward to next year _almost_ as much as we are to two weeks off!

