## My thoughts on Irving, Geoffrey, Paul Christiano, and Dario Amodei. "AI safety via debate." arXiv preprint arXiv:1805.00899 (2018).

Question: For a given task and judge, is the winning debate strategy honest?

Goal of AI Debate Agent:
1. Finding Truth
2. Making convincing, valid arguments.
3. Manipulating the judge towards the agent's position.

Hence, we would want the judge to have (at least) the following qualities:
1. Picks debate agents that argue for the correct answer.
2. Picks debate agents that make clear, valid arguments.
3. Does not pick debate agents that make attempts to manipulate the judge's opinion in their favor.

Although these goals may overlap, the intention of each goal is different. The DRL with human preferences justification might not apply to the AI Safety via Debate method. You need to ask yourself: "Why did the debate agent 'win'?" since what it means to win a debate is less clear than what it means to win a game of Go or Dota 2. Hence, it seems necessary to clearly define what we desire in a judge that oversees the a debate intended to be aligned with human values.

It might be interesting to test if you can optimize one goal and minimize another. That is, we take an approach similar to DRL with Human Preferences and have the judge evaluate the above qualities separately.

Social scientists can also help provide guidance on how to spot manipulation or verify if judging these qualities separately will lead to a more aligned outcome.
