---
title: "Rebooting activity at the start of 2025!"
date: 2025-01-09
permalink: /weeknotes/2025/01/rebooting/ 
---

## Rebooting activity at the start of 2025

(JW) Trying to keep up the weeknotes activity as an opportunity for reflection... It's an odd time of year, with people trickling back in from annual leave at different rates. Our office is closed between Christmas and New Year, and in Scotland we have an extra bank holiday on Jan 2nd, so work's only restarted for me this Monday.

The week kicked off at a good pace, with a visit from [Noushin Eftekhari](https://noushineftekhari.github.io/) to one of our recurring meetings, to discuss and demo some of her work on plankton image classification, supported by the Turing Institute and in collaboration with CEFAS. Inspiring stuff of near-to-realtime access to image analysis on the boat that the samples are taken from (it's all marine plankton, where our local focus is freshwater). The talk briefly turned to [Reynolds values and this 2002 paper](https://academic.oup.com/plankt/article/24/5/417/1507791?login=true) - _Towards a functional classification of the freshwater phytoplankton_. No, I haven't made the time to read it and reflect on how unsupervised image machine learning methods could reflect its conclusions, but I'd like to!

There are still a lot of open questions about how a "sensor-agnostic" plankton model could be developed to make reasonably consistent predictions, or meaningful embeddings, about images captured from devices at a range of different resolutions. There's space here for a Variational Autoencoder as in the first phase of a diffusion model, but that's well out of my scope for engagement here - perhaps it can be part of a future UKRI application.

The immediate delivery focus for that project is image machine learning pipelines and there's another clear application for those in the FDRI project. I started turning out a rapid prototype for feature extraction from Phenocam images on Christmas Eve, and [polished it up a bit](https://github.com/ukceh-rse/fdri-phenocam) during this week. I want to be able to show unexpected analytical potential in using deep learning models for purposes they weren't designed for. I liked the results, and tried to make them as reproducible and well-documented as i could, but the outcome is too far away from the project's immediate needs for this year, which focus on semi-automating an existing manual approach while migrating it off on-premise infrastructure onto Amazon Web Services.

It's a very different style of project from most of what our team has been lucky to work on so far - a multi-year plan, support from project managers and product owners, big enough that technical choices are centralised and the balance between flexibility and consistency is hard to find. Its outline is all JIRA-based, and has been that way for some time; our team's recent efforts to trial Github Projects to present a kanban-style view of issues and keep each other informed, look as if they go against its grain. The rest of this note I wrote in team chat, and now unapologetically paste it here! (I probably feel too strongly about it, but that's JIRA for you...)

If "how and what to build remains under discussion" and JIRA is mainly being used for project management tracking rather than technical collaboration, then I feel more strongly about making the case for not coordinating implementation work there, but doing it close to the code and in a way that is accessible by "stakeholders" (which right now is Github Issues)
 
I've spent a lot of my working life in "structured systems", and have seen directly and multiply how PM-led tracker boards can lead easily to developer disengagement, erosion of morale and productivity, and ultimately retention problems. It seems so unnecessary to construct that way of working in the midst of a research culture which prioritises personal commitment to work and is good at doing that.
 
I can find autonomy and creative freedom in other areas of my life, what i care about in the workplace is _having a voice in decisions, feeling listened to, not having to tone police myself_ - that's a privilege everyone should be able to enjoy! Entering another part of the culture where one's viewpoint - technical or socio-professional - sticks out as different, and it's on you either to mask up or drive the change - it gets tiring after a while, picking one's battles is a form of conserving one's passion for when it's returned.

An odd note to end the week on, two weeks off is no time at all :)

