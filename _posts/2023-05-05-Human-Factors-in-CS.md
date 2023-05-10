---
title: Emapthy in HCI (CHI 2023 writeup)
layout: article
tags: Research
---

This blog post comes as a reflection of the past few months of my work
with empathy in conversational agents, in studying the relationship
between commonly understood words and academic demarcations of their use.
I would like to better appreciate the scope of human factors research, and
this writing exercise is an effort towards that.

<!--more-->

## Empathy and Conversational Agents

I had submitted a paper to the EmpathiCH workshop this year at CHI. A
young workshop, in its second edition, wished to explore empathy
centered design, wherein I presented a paper on the design and motivation
behind the EmpatheticDialogues corpus published by Meta.

Empathy is a confusingly complex topic. Beyond the rudimentary social
understanding of what empathy is, its roots in literature are so varied
and the methods by which it is currently studied are so divided, that
even such a simple word with a common social understanding becomes
difficult to operationalize in any meaningful capacity when viewed without
context.

"To relate to another's emotions as if they were your own", is not much more
than an adege, really. What is "relating"? How do we know if we are "relating"?
What are emotions and how do I know the difference between mine and others?
Beyond a consensus on the word-feel, if you will, the operationalization of
the term in the context of the interface between humans and technology has proven
to be a challenge in research.

This also begs the question: "Why?" Why do research in empathy? What exactly
does empathy help with in terms of a design decision that other human factors
do not? Why not, say, sympathy, compassion, or even inclusiveness? What is
the role of empathy in design?

I will start with the dialogue systems research that I am doing to better
frame this question. I am a long ways away from a convincing answer, but
this should provide some motivation towards thinking about that work.
Empathy is seen as a core characteristic of human interaction, and is
one of the factors for effective communication that allows the participants
to understand and relate to one-another better. In human-machine interaction,
conversational interfaces for general purpose conversation are limited
in their effective capacity to "communicate" with the user. Even with how
advanced modern AI like ChatGPT is, it is a far cry to say that it
is human-like in its conversational capability. In fact, it is still very
much a task-based system, where the tasks are contextually defined by the
user rather than by the design of the system. The concepts of empathetic
"building-a-rapport" type conversations are not in its forte.

Is having that barrier or relationship between huamns and AI necessarily
an undesirable thing? No, of course not (I intend to write a post on 
the anthropological reimagination of digital intelligence sometime in the future).
However, there is definitely a barrier and it is hypothesized that
empathy is one of the key components of effective human-machine interaction
because of the role it plays in effective human-human communication. 

The fuzzily defined stakeholders and mission are about enough to develop a
framework for such a system, but the weeds of it still need to be well-understood.
What is empathy impacting in the design pipeline? How is the data collected
to capture empathetic conversations? How is the algorithm developed around it?
How does it impact the results of the system? How does the agent process cues
associated with empathy? Is empathy a process or an outcome?

EmpatheticDialogues was a step in this direction, to develop a baseline to
answer these questions. And while the modeling of a system that uses emotional
cues and tagged data to generate more "empathetic/sympathetic" responses
seems like step in the right direction, the realization of empathy in the
presentation of the work seems flawed. You can read all about that in my paper,
but suffice to say that there are three main places where there is an issue:

- label collection: 32 emotions? How?
- data presentation: why are all the turns of the dialogue linked to the 
same emotion? why are the dialogue lengths so short? why is the first participant
so much more involved in the conversation?
- data implications: how are these dialogues "more empathetic" than other
dialogues? is there such a thing as more empathy?

## Empathy and HCI

Within HCI, empathy has a unique role and history. Initially starting out as
a tool for improving interactions or modifying them in high-stress and
emotion-laden scenarios including therapy and patient care, it began to be
introduced into more and more modern human-robot interactions, including
the embodied agents which were characteristically intended to have
human-like features or qualities including facial expressions, as well as
access to mutlimodal input including voice (and all the lovely tonal and 
prosodic information to come with that) as well as facial expressions.

Outside the context of care and therapy, empathy is being considered
as a deisgn principle, the idea that the design process accounts for the
context and associated emotion for the stakeholders for which a given
tool, interface, or experience is being designed. This could include
everything from using interfaces to evoke empathy from people who often use
gig-work (shoutout EmpathiCH organizer Wo Meijer et. al.) and empathic
building spaces including the development of calmer working and recreational
environments (presented by Shruti Rao) to detecting distress and emotion
evocation for malicious intent (Verena Distler et. al.'s work) and emotion
expression via mini robot gestures (Chen Ji et. al.'s paper and adorable
tiny robot demonstration).

Work that was presented at this workshop and in the CHI community at large
showcased two important realizations:

- **Empathy is multidimensional**: Empathy is a multidimensional construct. Not
that we needed proof of that (cf: cognitive, affective, and behavioural studies
and their decades long disagreement over emapthy and emotion contagion), rather
that when applying it in the context of humans interfacing with agents, or humans
interacting with other humans using such agents, different aspects and dimensions
of empathetic engagement with/using the agent become more relevant than others.

- **Empathy is contextual**: I want to use that word very carefully. Context is not
just the situation which preceded the emotionall-laden turn of dialogue, rather
the relationship the participants have with one-another, the time and place in
which the conversation is occuring, as well as many other tacit factors that
change the way humans communicate and present emotional information to one-
another. 

To combine them together, identifying the stakeholders that are going to be
affected by the inclusion of empathy in a system and then examining the role
empathy would play in the context of their relationship for the purpose of
design become very important in determineing whether or not empathy is
necessary or relevant in the process of designing the agent, where empathy
plays a significant role, and more specifically, how do we measure the
change in the agent behaviour due to this empathetic design component?