---
layout: single
title:  "A journey into effects"
date:   2021-09-26 03:29:00 +0200
categories: effects
---
State is an interesting topic, since it is one of those tools that seem intuitive on the surface, but rapidly become a very costly abstraction.

In pure functional programming, state in the traditional sense, is not available.
Fortunately, purity is does not necessarily lock us out of interacting with the real world!

Most useful programs should declare their intent, but inevitably have ulterior motives, say using a temporary file as an intermediate step of a lager set of computations.
Modelling arbitrary side-effects purely, requires one to 'move' the evaluation of an effect to some abstraction layer outside of the program, say a familiar type like `IO`.
Interestingly enough, mutable state and other impure constructs can also be encoded into a pure programming language.

1. The first topic will be the exploration and implementation of a pure encoding of an impure effect.

2. The second topic will leverage ideas from 1. to build the necessary primitives to solve further problems, such as state and synchronization.

3. The final topic will bring previously explored ideas together in a model that is of a _functional reactive programming_ nature to solve real problems.
