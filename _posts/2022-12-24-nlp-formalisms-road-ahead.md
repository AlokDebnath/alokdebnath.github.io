---
title: NLP, Formalisms, and the Road Ahead
layout: article
tags: Thoughts
---

Grammar formalisms are a method of formalising, understanding and representing
syntatic structures. They model the syntax and provide a rigid, comprehensive
and parsable notion of grammaticality in a given language.

<!--more-->

However, as a
sub-field of natural language processing and computational linguistics, research
in grammar formalisms has been rapidly declining if it can not be used in an
application: to the point where the study of the formal notion of language
syntax, as a theoretical study, has lost interest in the community.

Case in point: One of the only known *ACL workshops for formalisms was known as
TAG+ and was held once every two to three years after 1998. Looking at the
statistics of the number of papers in the [workshop proceedings](https://www.aclweb.org/anthology/venues/tag/),
we see that after 2004,
there has been a rapid and noticeable decline in the number of papers, and 2012
onwards, a majority of the papers became about developing taggers, super-taggers
and discourse structure (though languages like Arabic and Hungarian stayed in
the mix). TAG+ has not been held since 2017.

I understand that the nature of NLP is changing, and it has becomes about
solving problems rather than investigating theories, and that the nature of
theoretical study now expected would probably lean towards analyzing the neural
blackboxes rather than theoretical insights into language structure. In the
meantime, hoards of low resource languages with informally written grammars (and
almost no data for the *extremely specific* NLP tasks), will get pushed
farther and farther away from being included into the computational linguistics
circles in the systematic manner that they used to.

Telugu, Tamil and Malayalam are some examples of such languages. A potential
direction of future research could be to understand the viability of lexicalized
grammars for representing the syntax of these morphologically rich languages,
and understanding that syntactic formalism need to inculcate both dependency as
well as morphological information to provide insight into the "structure"
underlying the language and formalizing it.
