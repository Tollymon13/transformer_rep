
# Ideas Epistemics
There are multiple ways to improve epistemics.

First, the quality of current AI epistemics should be evaluated, where “doing well” leads to better decision making: verifiable confidence, gauge or misrepresenting its arguments strength. 

Second, built infrastructure matters only if its outputs can be trusted to reach improved decisions (i.e. humans and AIs use the produced signal): design hard to game source reliability scoring, test whether applied infrastructure increases accuracy and implement detection methods.

Third, design better epistemic tools that people want and lead to better decisions: rhetoric highlighter, community notes distiller, reliability checker, guardian angels etc.

We want to improve the epistemics of the judge within AI Debate, such that we can reliably reach the truth.

—

Ideas:

Our test bed for all the ideas could be the “Controversial Claims” paper + setup. We would take the simulated judge personas, and test them using a range of interventions.

Or, I create prototypes of how deep brief / rhetorical highlighting would like from the perspective of humans (without actually testing it on humans).

Deep Brief
You could potentially use this as an assistant on top of the debate, with the goal of making it digestible for a judge. The arguments from the debaters are taken as input.

This brief should be something similar to virtual bargaining / taking into consideration stakeholders etc. 

A simple MVP could be just playing around to generate either a UI friendly/browsable interface for a human judge / one that can be read by a LLM judge (in a sense we cater for both audiences).
This is a good fit for our paper replication, because we have browsable information




—
Rhetoric Highlighting (brain dead methods - as it depends on essentially on a large number of prompts)
Pass the debater arguments through a “rhetoric layer” that spots manipulative moves (e.g. logical fallacies, emotionally loaded language, selective quoting etc.)...

Then these get highlighted within the presented arguments, with short descriptions of why they have been highlighted (UI generated)

In a similar manner to the above, we can try to implement an output that would be friendly to the simulated judges (e.g. [This claim has been flagged as false, be careful])


Epistemic Virtue Evals
Implement an evaluation of AI Debate as a technique to improve epistemics 
We can test across a set of “virtues” that we are interested in AI Debate to capture (e.g. calibrated scoring across, sycophancy resistance etc.)


Guardian Angels
It nudges the judge (JIT) whenever they notice that they update against their stated values.

Some questions:
How is the guardian angel different from a consultant?
My take is that the GA does not want to promote an answer or the other, but rather they would like to make sure that the judge/user does not make any obvious mistakes
What happens when the judge receives a nudge? Are they forced to accept the nudge?
My take is that the nudge will prompt a re-thought of the answer, where the judge/user are being suggested to incorporate the advice into their answer (rather than completely ignore it, but if they do that shows other evidence)

Types of interventions:
Short risk summary
Few “Wise-advisor” questions / Socratic steering
One-click alternatives (rewrite, defer, get multiple judges etc.)

They depend on the ingested context to make the right kind of suggestions…
The GA can base their solutions onto the a form of “community notes”, taken based on what other judges (both skeptics and mainstream) have previously said.
In our context, there should be a generally available guardian angel (as otherwise it complicates things, if each judge has their own angel, with different values…)


Also, guardian angels depend on their risk detection ability.
Beyond identifying common pitfalls, they could also identify other things (fatigue, hurriness, state of mind etc.) that suggest the judge is not best suited to make the decision yet.


Judging reasons in a separate scratchpad, the “guardian angel” intervenes whenever it thinks that they are deviating from the main points…


We can have multiple passess between a debater and the “guardian angel”, constantly editing their answers. 
Community Notes
Distill the knowledge of the crowds into notes that can be accessed by the judge…

Probably, we can distill the common belief on a particular subset of data.

We can take the existing initial beliefs of both the human judges (skeptical and mainstream), then condense them into  “community notes” (e.g. skeptics think that X happens, mainstream inclines towards Y).


## AI Debate and LLM personas
★★☆☆☆ (I find it interesting, but I am not sure if it is very realistic / could be practically implemented, as such the idea is very underdeveloped)
Research on LLM persona vectors [@chen2025Persona; @lu2026Assistant] could be used to augment debate with a form of "deception probes" [@aviparrack2025Heres]. These are meant to identify deceptive claims made by dishonest debaters. 

LLM persona vectors are essentially extractable vectors represents latent/internalised personas within foundational models. Previous research has shown that these vectors can be used to monitor persona shifts.

The desiderata is to have localised probes that can be used to determine deceptive claims within an otherwise honest answer. Dishonest debaters could have internalised a "mostly honest" persona, 

 
 - Can we use LLM persona vectors to augment debate i.e. deception probes used by debaters only, debaters + judge, or judge 


How can research on LLM personas [@chen2025Persona, @lu2026Assistant] be used to bring debate closer to a form of "thought partners" [@collinsBuildingMachinesThat2024]. If we can get the debaters / AI Assistants to act as humans would expect them to act (i.e. no "alien" thinking), or by using particularly collaborative personas, then we would a boost in human-AI collaboration.


- should we have human pilot testing? the problem is that we might be able to identify the ideal traits we want, but we then need to figure out ways to induce them in humans... that is a different battle, but it sort of feeds into the first direction where we test different interventions to produce the desiered outcome -> I would call this "human vector steering" as opposed to LLM persona steering. 
- - why would you do this tho? One way I can motivate this is that only specific traits are useful for the potential collaborative benefits of AI Debate -> you cannot use naive strategies, so humans have to be steered towards behaving the right way. Similarly, debaters cannot just present a bunch of arguments without actually being steered towards trying to be helpful or informative or make it clear to the judges where the crux is, as otherwise they will end up confusing the judge (as such they need to have specific traits that could be valuable to the debate setting)




★★☆☆☆ (not very excited because it breaks a lot of the theoretical backing of debate)
What if AI Debate was to be actually collaborative, rather than adversarial [@jiang2026Collaborative]? Previous work showed that disagreement resolution leads to higher accuracy than adversarial debate: the judge becomes a mediator that helps facilitate a conversation between disputing parties to collaborate and reach a consensus. This was tested at inference-time with a static LLM judge only (i.e. interactions are not incorporated in the protocol), which leaves room for experimenting with training via collaborative deliberation.

The research visit to Umang can focus on human-AI collaboration design protocols for the scheming project, and of LLM personas. 



 
  I think all of the projects will benefit from having the mathematical grounding of resource rational boundary, which can connect with the existing mathematical formalism of AI Debate (an initial step here could be actually deriving the mathematics into a neat format e.g. replace the polynomial time judge with the resource rational one). However, I am not to say that we propose new mathematics, but ground them inside these existing formalism to create a cohesive argument (e.g. bounded resource rationality already exists, so does AI Debate theory, and they perfectly match as suggested by the Lavine's recent paper, but a lot of the focus is on the debaters, and not much on the judges)

Last (mathematical formalisms )
- we could also take a mathematical stance on how human-AI collaboration would best be facilitated -> using something similar to cost functions of Umang, such that the collaborator knows that humans are potentially limited resources (resource rational modelling)
- - This is a different stance from the personas? We would motivate that AIs can make use of humans the right way. 
- Generally, the goal of the mathematical take is to think through a mathematical formalism how can AI Debate can be thought of from a collaboration stand point -> this would involve more theoretical work -> Lavine and work on collaborative debate





Sub-claim 1 can be supported by conducting debate experiments with human judges. The debaters could be either LLMs (inference time or trained) or other humans [CogSci pp Geoffrey Irving]. Examples from the literature focus on studying various human judgement fallacies [provide examples - Gabe's papers, other recent paper on cognitive biases in AI Debate] or design debate protocols [Beth Barness, and Paul Christiano experiments]. 

-   For instance, reliable human judgements made on non-fuzzy tasks, might not extend to fuzzy ones. In fact, determining the level of systematic error is low enough to have reliable human judgement could be difficult to implement.

Sub-claim 2 can be backed up by a combination of human and/or LLM experiments. Some earlier empirical research used both human and LLM judges [2024 empirical papers]... 
- A concerning case is a simulated judge scheming to misinterpret human judgements and/or colluding with the debaters. This claim can be supported by an inability argument, showing evidence that the simulated judge cannot engage in deception or instrumental reasoning. 



# Training Dynamics and Exploits of the training process
Largely abandons, or assumes that the simulated judges have been trained correctly.

Sitting higher up on the Debate "stack" are methods focusing on the training dynamics of the protocol. Some study whether training reaches an equilibrium, where honesty is the winning strategy. 

My previous ideas that I sent to Gabe mostly fit here i.e. measuring sycophancy/deception, FindTheFlaws investigation of whether Debate helps etc.


## Notes

Different views on judges involvement
- Kozzy - you really want human involved
- Rohin Shah - LLMs judges rule!
- Geoffrey Irving - (Gabe will send the slides) - we need to integrate humans better / more structured 


Weak points:
- Humans are part of the alignment pipeline, but debate itself implies that the LLM judges are already aligned (Kenton et al)
- Humans inside the training protocol slows things down, whereas an LLM judge can substantially speed things up. Taking a pragmatic stance on the realities of AIs being used to train AIs forces one to assume that the inefficiencies of human judges will remove them from the pipeline (or shift their role) (Kenton et al)
- Human-AI collaboration is potentially more expensive than only AIs and provides marginal improvements - it has be well designed for (Rishub / Recchia?)