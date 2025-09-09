# Evaluation Tools and Metrics for Generative AI
## How Do We Know If Our AI Is Actually Good?

---

## The Problem Statement

Imagine you've just built the next ChatGPT. 🤖

Your AI can write essays, answer questions, and even compose poetry.

But here's the million-dollar question: **How do you prove it's better than the competition?**

---

## Why This Matters

* Companies spend millions on AI development
* Users need reliable, high-quality AI systems
* Researchers need to measure progress
* **You need objective ways to compare AI performance**

Without proper evaluation, we're just guessing! 🎲

---

## Our Journey Today

1. **N-gram Metrics** - BLEU & ROUGE
2. **Embedding-based Metrics** - BERTScore
3. **Learned Metrics** - BLEURT
4. **Human Evaluation** - MQM Framework
5. **Combining Approaches** - The complete picture

---

# Module 1: N-gram Based Metrics
## The Foundation of Automatic Evaluation

---

## Why Automatic Metrics?

**The Challenge:** Human evaluation is:
- ⏰ Time-consuming
- 💰 Expensive
- 🔄 Hard to reproduce
- 📏 Subjective

**The Solution:** Automatic metrics that can:
- ⚡ Run instantly
- 💸 Cost almost nothing
- 🔁 Give consistent results
- 📊 Provide objective scores

---

## Enter BLEU Score

**BLEU** = **B**i**l**ingual **E**valuation **U**nderstudy

Created by IBM in 2002 for machine translation evaluation.

**Key components:**
- n-gram precision (1-4 grams)
- Brevity penalty (to prevent gaming with short outputs)

[📖 Original BLEU Paper](https://aclanthology.org/P02-1040.pdf)

---

## BLEU: The Core Idea

BLEU measures **precision** of n-grams (word sequences):

**Reference:** "The cat is on the mat"
**Candidate:** "The cat is on the"

**1-gram precision:** 5/5 = 100% ✅
**2-gram precision:** 4/4 = 100% ✅

*But wait... something's missing!* 🤔

---

## BLEU in Action: Simple Example

**Reference:** "I love machine learning"
**Candidate 1:** "I love machine learning" → BLEU ≈ 1.0 🎯
**Candidate 2:** "Machine learning I love" → BLEU ≈ 0.6 📉
**Candidate 3:** "I hate machine learning" → BLEU ≈ 0.7 🤷

*Why these scores? Let's find out!*

---

## 🚀 Call to Action: Hands-On Time!

**Open your workshop notebook now!**

👨‍💻 **Exercise 1:** Calculate BLEU scores for different text pairs
- Experiment with word order
- See how BLEU reacts to synonyms
- Discover BLEU's limitations

**Time:** 7 minutes

---

# Module 2: ROUGE Metrics
## A Better Tool for Different Tasks

---

## BLEU's Limitation

**BLEU Problem:** Only measures precision, ignores recall

**Example:**
- **Reference:** "The quick brown fox jumps over the lazy dog"
- **Candidate:** "The fox" 
- **BLEU:** Relatively high (both words match!)
- **Reality:** Missing 80% of the content! 😱

---

## Introducing ROUGE

**ROUGE** = **R**ecall-**O**riented **U**nderstudy for **G**isting **E**valuation

Developed for summarization tasks by Chin-Yew Lin (2004).

[📖 ROUGE Paper](https://aclanthology.org/W04-1013.pdf)

---

## ROUGE Variants

**ROUGE-1:** Unigram overlap (individual words)
**ROUGE-2:** Bigram overlap (word pairs)
**ROUGE-L:** Longest common subsequence (LCS)
**ROUGE-W:** Weighted longest common subsequence

**Focus on ROUGE-L:**
- Identifies longest sequence of matching words
- Order matters, but words don't need to be consecutive
- More flexible than fixed n-grams

*Each serves different evaluation needs!*

---

## N-gram Metrics: Strengths & Limitations

**Strengths:**
- ✅ Simple, fast, and reproducible
- ✅ No training required
- ✅ Language-agnostic (mostly)
- ✅ Correlate reasonably with human judgment on some tasks

**Limitations:**
- ❌ Insensitive to synonyms and paraphrases
- ❌ Penalize word order changes even when meaning preserved
- ❌ Miss semantic similarity
- ❌ Poor for creative generation tasks

## ROUGE vs BLEU: Key Differences

| Aspect | BLEU | ROUGE |
|--------|------|-------|
| Focus | Precision | Recall |
| Best for | Translation | Summarization |
| Measures | N-gram overlap | Various overlaps |
| Penalty | Brevity | None |

---

## ROUGE in Practice

**Original Text:** "Artificial intelligence is transforming how we work, learn, and communicate in the modern world."

**Summary 1:** "AI transforms work and communication."
**Summary 2:** "Technology changes everything."

*Which summary is better? Let ROUGE decide!*

---

## 🚀 Call to Action: ROUGE Workshop

**Back to your notebook!**

👨‍💻 **Exercise 2:** Compare summaries using ROUGE
- Calculate ROUGE-1 and ROUGE-L scores
- Analyze different summary qualities
- Compare with your intuition

**Time:** 8 minutes

---

# Module 2: Embedding-Based Metrics
## Going Beyond N-grams

---

## Why N-grams Aren't Enough

**Example:**
- **Reference:** "The movie was excellent."
- **Output 1:** "The film was excellent." (Should be high score)
- **Output 2:** "The movie was terrible." (Should be low score)

**BLEU/ROUGE:** Output 2 scores higher than Output 1! 🤦

**We need metrics that understand meaning!**

---

## Enter BERTScore

**BERTScore** uses contextual embeddings from pre-trained language models (BERT).

**How it works:**
1. Convert words to vectors using BERT
2. Calculate cosine similarity between vectors
3. Find best matches between reference and candidate words
4. Compute precision, recall, and F1 scores

[📖 BERTScore Paper](https://arxiv.org/abs/1904.09675)

---

## BERTScore in Action

**Reference:** "The movie was excellent."
**Output 1:** "The film was excellent." (High BERTScore ≈ 0.95)
**Output 2:** "The movie was terrible." (Low BERTScore ≈ 0.75)

**Why it works:** "film" and "movie" have similar embeddings!

---

## BERTScore: Strengths & Limitations

**Strengths:**
- ✅ Captures semantic meaning and paraphrases
- ✅ Contextual understanding of words
- ✅ Higher correlation with human judgments

**Limitations:**
- ❌ Slower than n-gram metrics
- ❌ Depends on pre-trained model quality and biases
- ❌ Requires more computational resources

---

## 🚀 Call to Action: BERTScore Workshop

**Back to your notebook!**

👨‍💻 **Exercise 3:** Compare BERTScore with BLEU/ROUGE
- See how it handles paraphrases and synonyms
- Compare scores on examples where n-gram metrics fail
- Understand when to use embedding-based metrics

**Time:** 7 minutes

---

# Module 3: Learned Metrics
## Training Models to Evaluate Like Humans

---

## The Evolution of Metrics

**Traditional Metrics** → **Embedding Metrics** → **Learned Metrics**

**Why learn from humans?**
- Human evaluation is still the gold standard
- Different aspects matter for different tasks
- Automatic metrics should predict human preferences

---

## Introducing BLEURT

**BLEURT** = **B**ilingual **E**valuation **U**nderstudy with **R**epresentations from **T**ransformers

Developed by Google Research (2020).

**How it works:**
1. Start with a pre-trained BERT model
2. Fine-tune on millions of synthetic examples
3. Further fine-tune on human annotations

[📖 BLEURT Paper](https://arxiv.org/abs/2004.04696)

---

## BLEURT: Strengths & Limitations

**Strengths:**
- ✅ Highest correlation with human judgments
- ✅ Robust to noise and edge cases
- ✅ Can be customized for specific tasks

**Limitations:**
- ❌ Requires fine-tuning
- ❌ Less interpretable (black box)
- ❌ Computationally intensive
- ❌ May inherit biases from training data

---

## 🚀 Call to Action: Learned Metrics Workshop

**Back to your notebook!**

👨‍💻 **Exercise 4:** Explore BLEURT scores
- Compare with other metrics
- Analyze correlation with intuition
- Discuss when to use learned metrics

**Time:** 5 minutes

---

# Module 4: Human Evaluation
## When Machines Aren't Enough

---

## Why Humans Still Matter

**Automatic metrics miss:**
- 🎭 Fluency and naturalness
- 🧠 Coherence and logic
- 🎯 Relevance to context
- 💭 Creativity and style
- 📚 Factual accuracy

*Some things only humans can judge properly!*

---

## The MQM Framework

**MQM** = **M**ultidimensional **Q**uality **M**etrics

A standardized framework for human evaluation.

**MQM-lite:** Simplified version with three key dimensions:

1. **Adequacy:** How well is the original content preserved?
2. **Fluency:** How natural and grammatically correct is the text?
3. **Consistency:** Is the text internally coherent and consistent?

---

## Types of Human Evaluation

**1. Likert Scales**
- Rate from 1-5 or 1-7
- "How fluent is this text?"

**2. Pairwise Comparison**
- "Which text is better, A or B?"
- More reliable than absolute ratings

**3. Ranking Tasks**
- Order multiple options from best to worst

---

## Human Evaluation Challenges

**😴 Annotator Fatigue**
- Quality decreases over time

**🎭 Subjectivity**
- Different people, different opinions

**💰 Cost & Time**
- Expensive and slow

**📊 Inter-annotator Agreement**
- How much do evaluators agree?

---

## Best Practices for Human Evaluation

✅ **Clear Guidelines:** Detailed instructions for evaluators
✅ **Multiple Annotators:** At least 3 people per item
✅ **Quality Control:** Regular agreement checks
✅ **Balanced Design:** Randomize order, avoid bias
✅ **Pilot Testing:** Test your evaluation setup first

---

## 🚀 Group Activity: Human Evaluation with MQM

**Let's evaluate two AI-generated texts!**

👥 **Your Task:**
1. Form groups of 3-4 people
2. Read both texts in your notebook
3. Rate them using MQM-lite framework:
   - Adequacy (1-5)
   - Fluency (1-5)
   - Consistency (1-5)
4. Discuss your ratings with your group
5. Record your scores in the notebook

**Time:** 10 minutes

---

# Module 5: The Complete Picture
## Combining Multiple Metrics

---

## The Correlation Question

**Key Insight:** Good automatic metrics should correlate with human judgment!

📊 **Research Shows:**
- BLEU correlates ~0.4-0.6 with human scores
- ROUGE correlates ~0.5-0.7 for summarization
- Correlation varies by task and domain

---

## When to Use What?

**N-gram Metrics (BLEU/ROUGE):** Quick development cycles, basic quality checks
**Embedding Metrics (BERTScore):** When semantic understanding matters
**Learned Metrics (BLEURT):** High-stakes evaluation, when human correlation is critical
**Human Eval (MQM):** Final validation, nuanced quality assessment
**Combined:** Multi-metric approach for comprehensive evaluation!

---

## 🚀 Final Challenge: The Aha Moment

**Back to your notebooks for the grand finale!**

👨‍💻 **Exercise 5:** Compare all metrics with human ratings
- Plot human MQM scores vs. all automatic metrics
- Find cases where they agree/disagree
- Discover which metric best matches human judgment

**Time:** 8 minutes

---

## Real-World Applications

**🏢 Industry Examples:**
- Google Translate uses BLEU for development
- News summarization systems rely on ROUGE
- ChatGPT was trained with RLHF (Reinforcement Learning from Human Feedback)
- Google uses MQM for translation quality assessment

**📊 Modern Trends:**
- Embedding-based metrics becoming standard
- Learned metrics for high-stakes systems
- Human feedback integrated into training loops
- Multi-dimensional, task-specific evaluation frameworks

---

## Key Takeaways

1. **No single metric is perfect** - Use multiple approaches
2. **Context matters** - Choose metrics for your specific task
3. **Humans are irreplaceable** - For fluency and creativity
4. **Automatic metrics are practical** - For development and research
5. **Correlation is key** - Good metrics should match human judgment

---

## What's Next?

🔬 **Emerging Metrics:**
- COMET: Neural model trained on human judgments
- MAUVE: Distribution-based metrics for open-ended generation
- UniEval: Unified framework for evaluating multiple aspects
- Task-specific evaluation frameworks
- Human-in-the-loop continuous improvement

📚 **Further Learning:**
- Experiment with different metrics
- Read recent evaluation papers
- Build your own evaluation pipeline

---

## Questions & Discussion

**What challenges have you faced in evaluating AI systems?**

**How might you apply these metrics in your own projects?**

**What other aspects of AI do you think are hard to evaluate?**

---

# Sources & References

---

## Key Papers

![BLEU Paper](https://aclanthology.org/P02-1040.pdf)
**BLEU: A Method for Automatic Evaluation of Machine Translation** (Papineni et al., 2002)

![ROUGE Paper](https://aclanthology.org/W04-1013.pdf)  
**ROUGE: A Package for Automatic Evaluation of Summaries** (Lin, 2004)

![BERTScore Paper](https://arxiv.org/abs/1904.09675)
**BERTScore: Evaluating Text Generation with BERT** (Zhang et al., 2019)

![BLEURT Paper](https://arxiv.org/abs/2004.04696)
**BLEURT: Learning Robust Metrics for Text Generation** (Sellam et al., 2020)

---

## Additional Resources

📹 **Video Explanations:**
- [BLEU Score Explained](https://www.youtube.com/watch?v=DejHQYAGb7Q)
- [Human Evaluation in NLP](https://www.youtube.com/watch?v=8rXD5-xhemo)

📖 **Tutorials:**
- [Hugging Face Evaluate Library](https://huggingface.co/docs/evaluate/)
- [NLTK BLEU Implementation](https://www.nltk.org/api/nltk.translate.bleu_score.html)

---

## Thank You!

**Ready to evaluate AI like a pro? 🚀**

Remember: The best evaluation combines multiple perspectives—automatic metrics for efficiency, humans for nuance.

*Keep experimenting, keep learning!*
