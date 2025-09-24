# Reasoning Answers
## Question 1: Limited Data Improvement
**If you only had 200 labeled replies, how would you improve the model without collecting thousands more?**
- **Augment data** using LLMs for synthetic examples and paraphrasing.
- **Fine-tune a pre-trained model** (e.g., BERT) to leverage transfer learning.
- Use **active learning** to prioritize labeling uncertain predictions.


## Question 2: Bias and Safety Prevention
**How would you ensure your reply classifier doesn't produce biased or unsafe outputs in production?**
- **Audit for bias** using tools like Fairlearn or Aequitas.
- **Test adversarially** to identify edge cases and unsafe outputs.
- **Filter outputs** with rule-based or ML-based safety checks.

## Question 3: Personalized Cold Email Generation
**Suppose you want to generate personalized cold email openers using an LLM. What prompt design strategies would you use to keep outputs relevant and non-generic?**
- **Use structured prompts** with clear constraints (e.g., "Avoid clichés").
- **Include dynamic placeholders** (e.g., "[prospect’s recent achievement]").
- **Provide examples** of desired tone and anti-examples for guidance.
