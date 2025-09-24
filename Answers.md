# Reasoning Answers
## Question 1: Limited Data Improvement
**If you only had 200 labeled replies, how would you improve the model without collecting thousands more?**

To produce more training instances, I would employ data augmentation strategies like paraphrasing preexisting responses and creating synthetic data using larger language models.  I would also use few-shot learning or fine-tuning a pre-trained model, which makes use of existing knowledge to get good performance with little labelled data.


## Question 2: Bias and Safety Prevention
**How would you ensure your reply classifier doesn't produce biased or unsafe outputs in production?**

I would put in place multi-layered safety precautions, such as content filtering systems, bias testing across demographic groups, and a variety of training data.  Ongoing safety and equity would be guaranteed by routine auditing using red-team testing, human oversight for edge cases, and production output monitoring for detrimental tendencies.

## Question 3: Personalized Cold Email Generation

In order to avoid using generic language, I would employ structured prompts that include explicit limits and particular context variables (the recipient's role, firm, and industry).  Relevance and personalisation would be guaranteed if the prompt included specific examples of effective versus generic openers and clear instructions to relate to particular recipient information.
