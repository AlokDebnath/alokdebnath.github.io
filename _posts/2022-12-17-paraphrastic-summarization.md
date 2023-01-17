---
layout: article
title: A New Way to Summarize
tags: Research Ideas
---
_Thank you to Dr. Manish Shrivastava (aka manshri) for this idea. I have
not had the time to implement it yet, but one of these days, I shall
try my best to find some time to try to implement this. In the meantime,
here are 2 AM thoughts._

<!--more-->

## Summarization: A non-technical recap
A very common task in Natural Language Processing, automatic summarization
is a poster-child of secondary ML engineering markets who thought the
machine translation space was too crowded, but still wanted to stick with
a task that could neatly fit into Bahadanu et. al. (2015). Fundamentally,
given a piece of text, summarization is the ability to preserve semantic
information while using a fraction of the number of words in the
original text. The task, which evolves from the common, colloquial even,
notion of "summing up a &lt insert type of discourse here &lgt", is not
an unheard of term, and due to its deceptively simple description and
appeal to everyday life, is a common task for the publication of several
publications each year since 2007 at *ACL and other notable computational
linguistics and NLP conferences.

Of course, this introduction was unnecessary, and conveys only the fact
that I seem to be very bitter about this task. And this is true, but not
because summarization is not a useful task. The ability to capture semantic
information in a manner that it can be represented with a varying number
of words; that is the dream of representation learning in NLP. The idea
that the relevency and semantic importance of a given word to the overall
meaning of a passage can be captured is inherently a very bold claim,
considering the structure and flow of information in discourses. Even if
the claim only extended to a fraction of the natural language landscape,
say only factual reports in a given style, the ability to capture and
separate semantic information well enought to generate a sequence of
equivalent or comparable meaning is not a trivial achievement. To some
degree, it suggests that semantic information **can exist** in a space
outside that of words, and even if we have not mastered the art of
composition via mathematical operations yet, we are able to replicate
that semantic information using a different set of words.

However, this is not what summarization in NLP achieves. It is not created
or meant to achieve this goal either. Rather, it is meant to do be a
corollary to the machine translation task, a sequence-to-sequence task
which captures "the meaning" of a long string and produces a different,
albeit shorter string, with external constraints on length and ratio. To
top it off, machine leanrning models for summarization are evaluated on
ROUGE. Yes, the n-gram similarity ROUGE. Yes, the ROUGE which had to have
variations to accomodate for machine translation, and still does not
capture nearly enough semantic content to be a reasonable measure.

In an NLP world where semantic textual similarity is an overdone task, where
methods for the representation and comparison of similarity is already an
existing construct, why is it that we yearn to learn the best ROUGE score model?


Introducing: Paraphrastic summarization

## Paraphrastic Summarization

Let's take a more friendly detour into the NLP task of paraphrasing.
Evaluated using cosine and dot-product similarities, paraphrasing
is a sequence-to-sequence task which is based on perserving sentence
semantics while changing the vocabulary and syntactic structure as
much as possible.

Much like summarization, the goal of a trained paraphrasing model
is to retain the meaning of a given input sentence. And, it is
evaluated using the measures of the representation, aka vector
similarity. Of course, improving the method of evaluation is
a valuable line of research, but atleast it _pretends_ to evaluate
on something which is not "is my model able to copy and paste the
right words?".

To break down paraphrastic summarization into current NLP tasks would be
to reimagine summarization as a combination of "here are important words"
and "here is the best phrasing for these words". Therefore,
- Our task is to reconstruct a model of summarization, where the output
is a paraphrase of an extractive summary.
- To do this, the primary goal is to rethink the semantics of a passage
in terms of n-gram vectors rather than just n-gram words.
- Therefore, three simultaneous tasks arise, which include abstractive
summarization, paraphrase generation, and sentence similarity estimation.

The ideal model pipeline would be something along the lines of:
```
+-------------+         +-----------------+        +-----------------+
| long form   | ----->  | SummModel gen.  | -----> | Paraphrase the  | ------> cos (gen. summ., corp. summ.)?
| input text  |         | a summary       |        | sumamry         |
+-------------+         +-----------------+        +-----------------+
```

One method of implementing this would be to train a paraphrasing model,
then take the summaries in the corpus and paraphrase them into semantically
equivalent sentences. Create a sequence-to-sequence task whose main aim
would be to generate these paraphrased summaries, the output of which can be
measured with both the original summary and the paraphrased one via cosine/
other vector similarity measure. Another method could involve the use of VAEs
for the paraphrasing, and create a model where the BLEU score is _adversarial_,
while the cosine similarity score is metric. Then, use the sentence-BERT for
evaluation.

The possibilities are endless, and very hand-wavy in this post, I apologize.
My point being: let us please start using the metrics of the space we embed
our language in, to better understand what our neural models are capturing?
Is that too much to ask?
