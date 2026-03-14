---
layout: post
title: "Comments on ALife"
date: 2025-02-19
categories:
  - biophysics
  - artificial intelligence
  - artificial life
---

A while ago, WUR wrote an article on some of my postdoc work on animal learning and behaviour. One interested reader asked for my thoughts on the liked paper below. It focusses on whether a synthetic, computational version of an organism (such as an AI model, or an artificial organism - ALife) could learn about the world in the same way animals do. I thought it was a good paper, but did have some disagreements with the conclusions. The claims are substantial, and add to a very important debate in the intersection of computer science biology and biophysics. As I was asked to comment, I stuck my oar in and wrote some thoughts.

[How do organisms know what to do? Non-computability and the organism](https://www.frontiersin.org/journals/ecology-and-evolution/articles/10.3389/fevo.2021.806283/full)

I start here with summarising the paper for the benefit of my own understanding, and the reader's.

The core argument here is that operating in a changing environment requires more types of decisions than can be predicted ahead of time, because the natural world throws up mathematical ambiguities (bifurcation everywhere, mathematical chaos, etc). Therefore you need to be able to "learn" or "guess" responses to these tasks and ambiguities. They cannot be hard coded in a kind of decision tree. Navigating the world relies on "identifying and exploiting new affordances" "(opportunities or impediments on the path to achieving a goal)"

The authors argue that a biological nervous system is required for this, but an autonomous agent on silicon cannot in principle do this. The argument here is based on organisms being "Kantian wholes" (all the parts being in service of the thing).

On the surface, this looks convincing, however, several possible holes arise, especially when such a large claim is made. These mostly depend on how the argument affords a kind of "specialness" to life, and so I think the argument falls down as much on the side of the biology as the computer science.

1. Where does the central goal of an organism - continued existence self replication - emerge from? This is still an open question in the physics of the emergence of life (a big active topic in places like the Santa Fe Institute). And how is this any different from the cost function (the "goal") encoded in an AI, even if one is emergent and the other imposed?

2. There is an idea that traces all the way back to John Von Neumann from the 1950s that the nature of life itself is computational, and can even be described as an algorithm. This work is currently being revisited, with some convincing results by Blaise y Arcas at Google. ([Computational Life: How Well-formed Self-replicating Programs Emerge from Simple Interaction](https://www.rfsafe.com/wp-content/uploads/2024/08/Computational-Life-How-Well-formed-Self-replicating-Programs-Emerge-from-Simple-Interaction.pdf))
If this were the case, then that would throw out that idea that new affordances cannot be exploited by an algorithm that is computable on a universal Turing machine, as life itself would be doing this.

3. I am not entirely convinced by the argument about Turing machines and affordances. New affordances can be exploited probabilistically with feedback. New inferences can be modelled as conditioning future attempts at decision making on known information about situations that are "similar" in some way. I think the authors are either thinking too deterministically, and are being somewhat hand-wavy when talking about things like human creativity, assuming that there's definitely something more complicated than the above happening. I am open to correction by computer or cognitive scientists on this one though.

(1) and (2) are points on assumptions that are still totally to play for in the science of the emergence of life. I think (3) is more definitive and mathematical, but I would need to come up with a more solid argument for what I'm trying to say here. Issues (1) and (2) are kind of obliquely acknowledged in the third point in possible objections, where they state that the behaviour of AI agent might be indistinguishable from that of an organism. But what I'm saying is the inverse. Organismic behaviour may be indistinguishable from that of a sophisticated program that aims to replicate itself, in which case, the distinction breaks down, you just have some differences in hardware.

As an aside, the big issues I would see with AI on silicon is that you can encode *so much more* information in a useable way in tissue than silicon, and the space of configurations of tissue is so much larger than for a silicon chip.

I think one of the things that the paper gets at indirectly is that "you need noise" you can't just lock the model and have it be an AGI, unless it had **perfect information** available during training (the problem of much of mathematics after we discovered mathematical chaos, and the bane of all weather forecasters and climate modellers). And I think that's correct. You can't have determinism. Again though, from an engineering perspective, you don't always want to just let your model loose on the world and allow it to update itself in case it could be poisoned, or just degrade.

And I guess there's a kind of beauty there. The AGI would kind of have to be a living thing, and given that it could only ever consume/access new information at a finite rate less than that of the whole environment, it would risk consuming the wrong things and becoming less functional. And so then, even if you can say that life is computational, the AGI would need to have some properties that seem almost mortal.
