# Generative AI Evaluation Workshop 🤖📊

Welcome to the **Evaluation Tools and Metrics for Generative AI** workshop! In this session, you'll learn how to evaluate AI systems that generate text, like ChatGPT, translation models, and summarization tools.

## 🎯 What You'll Learn

By the end of this workshop, you'll be able to:
- **Master n-gram metrics** (BLEU, ROUGE) for quick evaluation
- **Apply embedding-based metrics** (BERTScore) for semantic understanding
- **Use learned metrics** (BLEURT) that mimic human judgment
- **Conduct human evaluation** using the MQM framework
- **Compare all metric types** and choose the right approach for your task

## 📁 Workshop Materials

This workshop consists of three main components:

### 1. 📊 Interactive Presentation
- **HTML Version (`presentation-slides/index.html`):** Full interactive slides with reveal.js
- **Markdown Version (`presentation.md`):** Backup text version
- Theory and concepts covering all metric types with real examples
- Contains "Call to Action" moments where you'll switch to the notebook

### 2. 💻 Hands-On Notebook (`genai_evaluation_workshop.ipynb`)
- **This is where you'll do most of your work!**
- Interactive exercises for BLEU, ROUGE, BERTScore, BLEURT, and MQM
- Comprehensive comparisons and visualizations
- Real "Aha!" moments comparing human vs automatic evaluation

### 3. 📚 Documentation (`docs/`)
- Instructor's guide and additional resources

## 🚀 Getting Started

### Prerequisites
- Basic Python knowledge (you'll be running code, not writing from scratch)
- A Google account (for Google Colab access)
- Curiosity about AI evaluation! 🧠

### Setup Instructions

#### Option 1: Google Colab (Recommended)
1. **Upload the notebook** `genai_evaluation_workshop.ipynb` to [Google Colab](https://colab.research.google.com/)
2. **Run the setup cells** at the beginning to install packages (NLTK, ROUGE, BERTScore, etc.)
3. **You're ready to go!** 🎉

#### Presentation Options
1. **Interactive HTML:** Open `presentation-slides/index.html` in any browser
2. **Markdown Fallback:** Use `presentation.md` if HTML doesn't work

#### Option 2: Local Setup
1. **Install Python 3.7+** on your machine
2. **Install required packages:**
   ```bash
   pip install nltk rouge-score matplotlib seaborn pandas bert-score jupyter
   ```
3. **Download NLTK data:**
   ```python
   import nltk
   nltk.download('punkt')
   ```
4. **Launch Jupyter:**
   ```bash
   jupyter notebook genai_evaluation_workshop.ipynb
   ```

## 📖 Workshop Flow

### During the Session:
1. **Follow the presentation** - Your instructor will guide you through concepts
2. **Switch to the notebook** when you see "🚀 Call to Action" slides
3. **Work in pairs or small groups** - Learning is more fun together!
4. **Ask questions** - There are no silly questions in AI evaluation
5. **Experiment freely** - Try to "break" the metrics and see what happens

### Workshop Timeline (75 minutes):
- **10 min:** Introduction & Setup
- **15 min:** N-gram Metrics - BLEU & ROUGE (8 min theory + 7 min hands-on)
- **15 min:** BERTScore - Embedding Metrics (8 min theory + 7 min hands-on)
- **10 min:** BLEURT - Learned Metrics (5 min theory + 5 min hands-on)
- **15 min:** Human Evaluation with MQM (5 min theory + 10 min group activity)
- **10 min:** Final Comparison & "Aha!" Moment
- **5 min:** Q&A and Wrap-up

## 🎪 Interactive Activities

### Activity 1: N-gram Metrics Exploration
**Time:** 7 minutes  
**What you'll do:** 
- Calculate BLEU and ROUGE scores for different text pairs
- Experiment with word order changes and synonyms
- Discover n-gram metrics' strengths and limitations

**Challenge Question:** Why do n-gram metrics struggle with paraphrases?

### Activity 2: BERTScore vs N-grams
**Time:** 7 minutes  
**What you'll do:**
- Compare BERTScore with BLEU/ROUGE on challenging examples
- See how embedding metrics handle synonyms and paraphrases
- Understand when semantic understanding matters

### Activity 3: BLEURT Exploration
**Time:** 5 minutes  
**What you'll do:**
- Explore BLEURT scores on various text pairs
- Compare all four metric types side by side
- Understand when learned metrics are worth the complexity

### Activity 4: Human Evaluation with MQM
**Time:** 10 minutes  
**What you'll do:**
- Form groups of 3-4 people
- Rate AI-generated texts using MQM framework (Adequacy, Fluency, Consistency)
- Discuss disagreements and learn from different perspectives
- Record your ratings in the notebook

### Activity 5: The Final Comparison
**Time:** 8 minutes  
**What you'll do:**
- Compare your human MQM ratings with all automatic metrics
- Find cases where they agree and disagree
- Experience the "Aha!" moment about evaluation complexity

## 💡 Tips for Success

### Before the Workshop:
- [ ] Test your notebook setup (run the first few cells)
- [ ] Bring a curious mindset - evaluation is both an art and science
- [ ] Think of examples where you've had to evaluate quality (essays, movies, restaurants)

### During the Workshop:
- [ ] **Don't worry about perfect code** - focus on understanding concepts
- [ ] **Collaborate with peers** - different perspectives make evaluation richer
- [ ] **Take notes on surprising results** - these are learning opportunities
- [ ] **Ask "why" questions** - Why did this metric give that score?

### After the Workshop:
- [ ] Try the concluding challenge with your own examples
- [ ] Explore the cited papers for deeper understanding
- [ ] Apply these concepts to your own AI projects

## 🤔 Common Questions

**Q: I'm not great at Python. Will I be lost?**  
A: Not at all! The notebook provides all the code - you just need to run it and experiment with different inputs.

**Q: What if the automatic metrics disagree with my human ratings?**  
A: Perfect! That's one of the most important insights you'll gain from this workshop.

**Q: Which evaluation metric is the "best"?**  
A: There's no single best metric - it depends on your task, context, and resources. N-gram metrics for speed, embedding metrics for semantics, learned metrics for human alignment.

**Q: Can I use these techniques for languages other than English?**  
A: Yes! Though some metrics work better for certain languages. We'll discuss this during the workshop.

## 📚 Additional Resources

### Want to Learn More?
- **Papers:** Check the references in the presentation slides
- **Tools:** Explore Hugging Face's `evaluate` library for more metrics
- **Practice:** Try evaluating outputs from different AI models you use

### Troubleshooting
- **Notebook won't load?** Try refreshing or use Google Colab
- **Package installation errors?** The instructor has backup examples ready
- **Stuck on a concept?** Ask your neighbor or raise your hand!

## 🎉 Ready to Start?

1. **Open the notebook:** `genai_evaluation_workshop.ipynb`
2. **Wait for the presentation to begin**
3. **Get ready to discover how we measure AI quality!**

---

*"The best way to learn evaluation is to evaluate, compare, and question the results."*

**Let's dive in!** 🚀

## 📞 Need Help?

During the workshop:
- **Raise your hand** for technical issues
- **Ask your neighbor** for quick questions
- **Join the discussion** - your insights help everyone learn

After the workshop:
- **Check the documentation** in the `docs/` folder
- **Experiment with the notebook** on your own
- **Share your discoveries** with classmates

---

*Happy evaluating! May your metrics be meaningful and your models be measurable! 📊✨*
