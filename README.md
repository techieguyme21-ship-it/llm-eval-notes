# llm-eval-notes

What does “evaluation” mean in LLM pipelines? Why it’s harder than in traditional ML or software, and how to begin error analysis?
* Unlike traditional software, LLM pipelines do not produce deterministic outputs. Their responses are often subjective, context-dependent,   and multifaceted. A response may be factually accurate but inappropriate (i.e., the “vibes are off”). They may sound persuasive while       conveying incorrect information. These ambiguities make evaluation fundamentally different from conventional software testing and even      traditional machine learning (ML)

* Outputs from these systems are not just right or wrong — they can fail in more subtle ways. For example, a pipeline extracting              information from emails might misidentify a celebrity mentioned in the body as the sender, or generate a summary in the wrong format even   if the facts are correct.
  
* These are not simple bugs you can catch with unit tests; they reflect deeper issues of the following:
   * comprehension (not knowing your data or outputs at scale),
   * specification (underspecified prompts that force the model to guess)
   * generalization (unexpected failures on new inputs).
