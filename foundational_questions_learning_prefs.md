## My thoughts on Christiano, Paul F., et al. "Deep reinforcement learning from human preferences." Advances in Neural Information Processing Systems. 2017.

I enjoyed the paper by Christiano et al. because the notion of preference is simple and intuitive for humans to understand and use to make sure intelligent agents are aligned with human values. If DeepMind and OpenAI intend to continue using human preferences in future AI Safety projects, some foundational issues need to be addressed:
1. (Foundations and paradoxes) Let $$<_h$$ be some (currently undefined) notion of human preference and $$<_a$$ be the preference ordering of an intelligent agent. In the Christiano et al. paper, it seems that we want something like the following:

> "For all alternatives $$A_1$$ and $$A_2$$, if $$A_1 <_h A_2$$, then $$A_1 <_a A_2$$."

> If so, what exactly is $$<_h$$? Could it be an aggregate preference? Should either ordering be axiomatized with desirable properties we would want in rational agents? You are probably aware of some of the paradoxes of formal choice theory like Condercet's paradox (which says that individuals with transitive preferences can have an intransitive aggregate preference). Will the paradoxes of (human) choice theory carry over to agents that learn from human preferences? Some research has been done to get around these paradoxes but it would be interesting to see if it could be used in AI research.

2. (Verification) Is there a plan to empirically verify that agents that learn from humans have consistent preferences? Unfortunately, even if we had a clear and strong foundation for human preferences, evaluating the behavior of agents that learn from human preferences might be difficult. Currently, the field of psychology might be facing a replicability crisis. Psychologists like Michel Regenwetter (University of Illinois at Urbana-Champaign) and Caren Rotello (University of Massachusetts, Amherst) claim that our methods of interpreting experimental results in human decision making are deeply flawed. They both cite examples from previously published works that make conclusions from human decision-making experiments and show that their data do not necessarily imply their conclusions. For example, one widely used method psychologists use to show transitivity is Weak Stochastic Transitivity (WST), which says that a group of subjects have transitive preferences if the group prefers A over B at least 50% of the time and prefers B over C at least 50% of the time implies that the subjects prefer A over C at least 50% of the time. Again, one can use Condercet's paradox to show that this method is invalid. Without an underlying foundation for inferring choice behavior, even something as simple as counting choice tallies can provide opposing conclusions. Hence, when trying to gain knowledge on the complex nature of human rationality, a heuristic approach like assuming “The aggregate behavior is the same as the behavior of the individuals” is inadequate. This point is important if we want to verify that agents behave consistently with human preferences or extend preference-based RL to multi-agent settings.

Even if answers to these questions have not been solved yet, I still think using human preferences seems like a worthwhile endeavor and a necessary step towards AI that is aligned with human values.

Lingering Questions:

Is our end goal:  $$x >_h y$$ iff $$x >_a y$$?

What is $$>_h$$? Is it an aggregate preference? If so, do the same aggregation paradoxes arise?

Should we have the algorithm minimize a loss function that includes preference axioms?
