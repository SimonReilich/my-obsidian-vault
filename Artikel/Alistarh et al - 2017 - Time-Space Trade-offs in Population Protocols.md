---
title: Time-Space Trade-offs in Population Protocols
author:
  - "[[Dan Alistarh]]"
  - "[[James Aspnes]]"
  - "[[David Eisenstat]]"
  - "[[Rati Gelashvili]]"
publisher: "[[SODA - Symposium on Discrete Algorithms]]"
year: "[[2017]]"
file: "[[Alistarh et al - 2017 - Time-Space Trade-offs in Population Protocols.pdf]]"
sources:
  - "[[Angluin et al - 2006 - Computation in Networks of passively mobile Finite-State Sensors]]"
  - "[[Angluin et al - 2008 - Fast Computation by Population Protocols with a Leader]]"
  - "[[Angluin et al - 2008 - A simple population protocol for fast robust approximate majority]]"
  - "[[Alistarh et al - 2015 - Fast and exact majority in population protocols]]"
  - "[[Andoni und Razenshteyn - 2015 - Tight lower bounds for data-dependent locality-sensetive hashing]]"
  - "[[Bower und Bolouri - 2004 - Computational modeling of genetic and biochemical networks]]"
  - "[[Berenbrink et al - 2016 - Plurality consensus via shuffling]]"
  - "[[Chen et al - 2014 - Speed faults in computation by chemical reaction networks]]"
  - "[[Cardelli und Csiksz-Nagy - 2012 - The cell cycle switch computes approximate majority]]"
  - "[[Chen et al - 2013 - Programmable chemical controlers made from dna]]"
  - "[[Chatzigiannakis et al - 2011 - Passively mobile communicating machines that use restricted space]]"
  - "[[Doty - 2014 - Timing in chemical reaction networks]]"
  - "[[Doty und Soloveichik - 2015 - Stable leader election in population protocols requires linear time]]"
  - "[[Draief und Vojnovic - 2012 - Convergence speed of binary interval consensus]]"
  - "[[Laurenti et al - 2016 - Programming discrete distributions with chemical reaction networks]]"
  - "[[Mertzios et al - 2014 - Determining majority in networks with local interactions and very small local memory]]"
  - "[[Perron et al - 2009 - Using three states for binary consensus on complete graphs]]"
  - "[[Thachuk et al - 2015 - Leakless dna strand displacement systems]]"
---
#Artikel #Informatik 
# Abstract
[[Populationsprotokolle|Population protocols]] are a popular model of distributed computing, in which randomly-interacting agents with little computational power cooperate to jointly perform computational tasks. Inspired by developments in molecular computation, and in particular [[DNA]] computing, recent algorithmic work has focused on the complexity of solving simple yet fundamental tasks in the population model, such as leader election (which requires convergence to a single agent in a special “leader” state), and majority (in which agents must converge to a decision as to which of two possible initial states had higher initial count). Known results point towards an inherent trade-off between the time complexity of such algorithms, and the space complexity, i.e. size of the memory available to each agent. In this paper, we explore this trade-off and provide new upper and lower bounds for majority and leader election. First, we prove a unified lower bound, which relates the space available per node with the time complexity achievable by a protocol: for instance, our result implies that any protocol solving either of these tasks for $n$ agents using $O(\log (\log n))$ states must take $\Omega(n/\text{polylog}n)$ expected time. This is the first result to characterize time complexity for protocols which employ super-constant number of states per node, and proves that fast, poly-logarithmic running times require protocols to have relatively large space costs. On the positive side, we give algorithms showing that fast, poly-logarithmic convergence time can be achieved using $O(log^2 n)$ space per node, in the case of both tasks. Overall, our results highlight a time complexity separation between $O(\log(\log n))$ and $\Theta(log^2n)$ state space size for both majority and leader election in [[Populationsprotokoll|population protocols]], and introduce new techniques, which should be applicable more broadly.