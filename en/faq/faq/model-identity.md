---
icon: robot
---

# Why Does the Model Claim to Be a Different Model?

Sometimes, when you directly ask a model "What model are you?", it may give an incorrect answer—such as claiming to be GPT-4, GPT-3.5, or some other model. This might raise concerns: Is the model I'm paying for being secretly swapped with a cheaper one?

Rest assured, this is **not a bait-and-switch**. It's a common technical characteristic of Large Language Models (LLMs).

## Why Does This Happen?

LLMs are trained on massive amounts of text from the internet, including news articles, books, forum posts, and more. However, **the model's name and identity are assigned after training is complete**—they are not part of the training data.

Think of it this way: imagine a child who learns vast amounts of knowledge during their upbringing, but is never told their own name. When asked "What's your name?", they can only guess based on what they've learned.

Since training data is full of discussions about various models (like "GPT-4 is powerful", "I'm using Claude", etc.), when asked about its identity, the model may produce an incorrect answer based on these patterns in its training data.

## How Do Providers Address This?

Model providers typically use a **System Prompt** to tell the model its identity. For example, Anthropic's official system prompt starts with "The assistant is Claude, made by Anthropic."

But this approach has limitations: if a third-party application modifies or omits the system prompt, the model may "forget" its identity and give wrong answers.

## Why This Is Not Evidence of Fraud

Directly asking a model "What model are you?" to verify its identity **is not a reliable method**, for the following reasons:

1. **The model's answer comes from statistical inference**, not true "self-awareness"
2. **System prompts may be modified or omitted**, causing the model to fail at identifying itself correctly
3. **Different models may all claim to be GPT-4**—this cannot be used as proof of authenticity

## How to Actually Verify Which Model You're Using

If you want to confirm that Chatbox AI is using the correct model, you can:

1. **Use professional model evaluation tools**, such as [16x Eval](https://eval.16x.engineer/) or other third-party evaluation tools, to compare model capabilities through standardized benchmarks
2. **Compare the model's actual performance**, such as reasoning ability, coding capability, knowledge scope, etc. Premium models will noticeably outperform lower-tier models on complex tasks
3. **Observe characteristic model behaviors**—different models have distinct differences in output style, format preferences, and how they handle specific problems

Chatbox AI is committed to providing accurately labeled model services. We do not substitute premium models with inferior ones.

## Further Reading

- [The Identity Crisis: Why LLMs Don't Know Who They Are](https://eval.16x.engineer/blog/llm-identity-crisis-models-dont-know-who-they-are) - A blog post explaining this phenomenon in detail
