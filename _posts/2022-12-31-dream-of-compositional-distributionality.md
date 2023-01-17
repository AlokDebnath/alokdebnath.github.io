---
title: The Dream of Compositional Distributionality
layout: article
tags: Thoughts
---

In this blog post, I aim to explore, very rudimentarily, the notion of
compositional semantics, distributional semantics, the idea of compositional
distributionality, and why it is such a dream which would change interpretable
NLP systems if ever achieved.... and why it might not be achieved.

<!--more-->

Language is a famously complex phenomenon, notably so because of the notion of
meaning. A preliminary question about the nature of arbitrary meaning in
language has often been asked as follows:

 > At which level of orthographic or phonetic granularity is meaning  located?

For example, the word `gook` doesnt really mean anything in English, but both
`good` and `book` have meaning. So clearly, meaning must be in the letters `d`
in good and `b` in book, because without them, the word doens't really have a
meaning.

For more than obvious reasons, this argument is flawed. We know for a fact that
an individual letter or sound doesn't really have a meaning, but an arbirary
sequence does. The minimal meaningful unit of meaning in a language (known as a
morpheme) is independent of the number or sequence of interchangable sounds or
letters. It's just that some sequences have meaning in a language and some don't
(c.f. arbitrariness).

If that is the case, then what really is the point of studying semantics? As it
turns out, even if there are only some sequences that are meaningful, combining
meaningful units into larger units of meaning, from morphemes to words, form
words to sentences, from sentences to discourse, follows certain patterns in
various languages. These patterns can be abstracted and studied, which is what
makes the study of semantics interesting. Moreover, since language interacts
with, describes, and communicates into and within a world, context, and setting,
understanding the embedding and relationship between meaning and representation
is an interesting problem.

With this in mind, we look at two such notions of menaning representation in
context, and how they can possibly be combined into becoming one of the most
useful studies of language if computationally viable.

## Distributional Semantics

  > How do we find out what a word means, when all we have are other words?

Without the access to a significant lexicon/oracle, and the ability to interpret
languauge outside its own confines, (i.e. using external representation, world
knowledge, or even constructions from other words), the notion of meaning
becomes very difficult to extrapolate.

For example, what does the word `bat` mean? One might say that it is a small,
black, winged mammal which lives in certain biomes and consumes fruits, insects,
and/or animal blood. The ability to define this word assumes two things, one
that the entity provding this meaning already knows the meaning of every word in
the definition, and that the entity has access to a lexicon or dictionary. If
these abilities are   stripped, then we have no meaning for a word. Or do we?

A critical thing to keep in mind about language is that it seems to follow
certain patterns at a large scale. One of these patterns is syntax, the fact
that large meaningful units have some structure to them. Large collections of
words, for example, follow sentence strucutre. If we choose a given smallest
unit, what we can do is analyze those patterns to derive some notion of meaning.
Researchers using an analytical language like English (in the context of written
language, of course), chose words as their smallest unit.

Therefore, the meaning of a word was extracted based on the meaning of other
similar words which occured in very similar contexts. For example, the word
`bat` would be used often in the same contexts as the word `rat`, `mouse`,
`bird`, `ferret`, and therefore, the conclusion would be that all of these words
would be similar in meaning. So, to a distributional semanticist (forgive the
terminology), the question:

  > What is a bat?

would be answered as
  > Something very similar to a mouse, a bird, a rat, and a ferret.

Computational implementations of distributional semantics, mainly word2vec and
its many successors, psuhed the study of NLP forward a great deal. This is not
the blog post where I explore word2vec, althought I  would love to do so. Today,
the idea of distributional semantics is closely tied to its computational
representations, although the theory of it far preceeds the computational
representations.

## Compostional Semantics

> If we know the meanings of individual units, can we know the meanings of a larger form?

Compositional semantics argues that using the rules that bind the smaller units
together, we can learn the meaning of a larger composed form. For example, the
meaning of the sentence you are reading now depends on the sum of the meanings
of individual parts, held together based on the syntactic structure. This idea,
which posits that the meanings of larger components is more than just the
smaller subphrases, rather it is also the way they are arranged, lends insight
into the meaning within the structure of language.

Computationally, capturing syntactic structures had not been considered akin to
parsing meaning, for phrase structure grammar is just that, a grammar. However,
compositional semantics claims that it is more that composition is, in essence,
the ability to use structure to represent meaning, that the structure is the
difference between a meaningful arrangement of units and a meaningless
collection. Therefore, creating a reasonably parsable representation, one which
uses an underlying mathematical representation to generate more meaningful
patterns without the use of actual units, became a central principle of
compositional semantics. Therefore, a facet of studying compositional semantics
involved studying grammar formalisms, generatiing a structure that could be
recognized and understood as a skeleton to the language, on which the flesh and
meat of words would reside and flourish.

Some popular formalisms, such as tree adjoining grammars (TAG), Lambek Calculus,
Pregroup Calculus, Combintory Categorical Grammars (CCG), etc. provide insights
into the structure of language and how that structure allows words and phrases
to come together to elicit certain meaning. Fun fact, my thesis was actually on
extending pregroup calculus to represent some facets of Hindi grammar, which was
really fun to  work on.


## Compositional Distributional Semantics?

Imagine a world where the meanings of words are known to a system, and a method
to put them together to form larger units is also known to the system. Then in
that world, we could somehow create a method to combine the meanings of each
word using a well-founded representation of structure, and viola! We would have
the meaning of larger units through useful and precise calculations.

This is the promise of compositional distrbutional sematnics, the idea that
there exists a reasonable mathematical framework that captures the
representation of structure, and a space in which the minimal units are embedded
which can interact with this structure, or more specifically, be represented
within the structural framework and used to compute the meanings of sentences.
Under the hypotheses that compositionality is a useful representation of
language (which, I mean, there are several non-compositional phrases, and
pragmatics is still a large part of language, so...) and that distributionality
captures the meanings of words effectively based on their surroundings (we
already know that there are several problems with this, polysemy, function
words, and measuring similarity, to name a few), we can use a larger
mathematical object to represent the meaning of higher-order phrases.

And this is exactly what Coecke did in his 2010 paper: [*The Mathematical
Foundations of a Compositional Distributional Model of Meaning*][1]. The paper,
published at a time when `word2vec` **was not yet published**, developed a
vectorial embedding of words, and together with pregroup calculus as the
syntactic representation, used the notion of free categories to develop a
sentence representation that could be measured using category-theoretic
operations between the members of a category. And to me, this was phenomenal.
It was an interpretable, deeply intuitive, useful method of capturing meaning
from two useful models of thought. The idea did gain some traction, but beyond
some applications in discourse, it never really made it to any big league
conferences in NLP.

Why?

For starters, there are several issues with using vectors and pregroups, but the
use of category theory made this concept fundamentally extensible to a variety
of representations, including gaussian, hypersphere, holographic, Poincare, and
complex space embeddings. Any mathematical object that can be raised to a
category can be used for the word repreesentations, and any context-free or
mildly context-sensitive grammar representation can be used for the syntactic
attributes, so clearly, the issue does not lie with the extensibility of the
representation itself. There is the fact that each combination of word and
grammar representation needs to be computed individually, which is time and
research intensive, not to mention computationally rigourous. Moreover, the
final product is a mathematical object which embeds a sentence with no data...
and it shows. The sentences that these models can accurately represent are few
and far between, and even with additional work having been done on
non-compositionality, there is a long way to go for these models to be used for
what they are actually proficient in. If they are ever used that way. Seeing as
how language representations have eliminated formalisms from NLP already, I
don't doubt that this will remain an esoteric study. I do wish that a reasonable
model of extensibility be developed using this idea. I find it fascinating and
to see a hint of what the lanugage space looks like by constructing it as such
would be innovative and an integral step in interpretability in NLP research,
to say the least.

[1]: https://arxiv.org/pdf/1003.4394.pdf
