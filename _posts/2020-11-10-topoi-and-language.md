---
title: Topoi and Language Represetation
layout: post
---

It is no secret that the vector space is possibly the most convenient and yet one
of the most inadequete spaces for the representation of natural langugae. Despite
its enormous popularity as the choice representation, glaring unexplained questions
about the mechanism of embedding into the vector space adopted by the likes of
`word2vec` and `GloVe`, and the representations that followed (`fasttext` and `BPE`
for example, which do not consider words, just letter embeddings, and use
letter n-grams as a substitute for morphemes) have shown to be more efficent when
computing over neural networks which perform tensor calculus for "learning"
representations for downstream tasks.

When along came contextualized word representations and then language representations
which outperformed the existing baselines for pretty much any NLP task known to us
(thank you BERT), something was gained, and something was lost. One of the most powerful
representations, trained to be the best language model possible, which could now be
considered the future of mainstream representation learning in natural language, was gained.
ELMo, then BERT and every one of the variations that followed had a very specific take on
language modeling and its tasks, and while that take accounted for context, used a metric ton
of data and compute, and was overall the a marvel in NLP engineering, the linguistic basis
on which such a representation were to stand, and the mathematics that would bring that
representation to light, were both lost to the whims of F1 and BLEU scores. While esoteric
research into these continues, BERTisms provide the most insightful language models and
representations today, under the tensorial paradigm of computation.

Outside the familiar embrace of tensor-based embeddings, all other possible models of word
representation have a steep hill to climb. Tasks, corpora, models, insights, comparisons,
and most importantly, a reason for R2 to accept their paper are all at a loss. In the desolate
quagmire of non-vector and non-tensorial embeddings, the fringe use-cases and comparisons
of spherical, hyperbolic, and graph embeddings were explored between 2017 and 2020. All of
these works answer a question outside those in BERTisms, i.e. what does a non-vector space
have to offer? What properties of natural language can be well encoded and represented in
these spaces? For example, synonymy is non-commutative in natural language; which spaces can
represent this arbitrary phenomena of language while maintaining function as a word embedding
(i.e. being acceptable at intrinsic evaluation tasks such as similarity, analogy, etc.) Another
fairly unique property of language is the structural behavior of comparative and superlative units, 
and the constructions they occur with.

One such "linguistically inspired" question that I and a good friend, [@bollu](https://bollu.github.io)
have been desperately looking into: "What is this list of arbitrary yet encodable properties
of natural language? If such a list exists, is there a place to express them, and embed the
meaningful units associated with them?" @bollu introduced to Topoi as a "space to do math",
which I interpreted to mean "a place where the lost collection of heuristics can find a place
to rest and feel loved". Grothendieck's topoi have shown great promise in this regard, allowing
the construction of topoi-theoretic bridges between different branches of math, connecting them
through (what I can only describe as wonderous) similarities in their construction. Do I know what
that means? No. Does it sound cool? Absolutely.

In order to find a reasonable-enough way to study whether there exists such a mathematical construct
out there, which we can use to scope out the various properties of language at different levels
(morphological, syntacto-semantic, and discourse) in a singular and coherent representation, I have
embarked upon a long journey to understand these beasts called Topoi. With the almost-no-math I know,
this should be a fascinatingly wild ride, and I will try to use the wonders this study provides to
escape the BERTisms that plague the papers I read (and will probably continue to read for years to
come). I shall attempt to document what I can, as and when I can. 

The textbook we are going to be using is _Topoi: The Categorial Analysis of Logic (Dover Books on Mathematics)_
by Robert Goldblatt. Wish me luck, and wish @bollu strength, for I am a horrible student.
