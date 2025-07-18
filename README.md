# AI-WEEK-3

Part 1: Theoretical Understanding (40%)
1. SHORT ANSWER QUESTIONS.
Q1: Explain the primary differences between TensorFlow and PyTorch. When would you choose one over the other?
- PyTorch uses a dynamic computation graph while TensorFlow traditionally used a static computation graph


Q2: Describe two use cases for Jupyter Notebooks in AI development.
-Interactive Model Prototyping and Experimentation
-End-to-End AI Workflow Documentation


Q3: How does spaCy enhance NLP tasks compared to basic Python string operations?
1. Linguistic Intelligence vs. Raw Text Manipulation
- spaCy understands language structure—offering tokenization, part-of-speech tagging, named entity recognition, and dependency parsing.
 2. Built-in NLP Pipeline
- spaCy provides a modular pipeline that processes text step-by-step: tokenization → tagging → parsing → entity recognition.
3. Speed and Efficiency
- spaCy is written in Cython, making it lightning-fast and memory-efficient—ideal for large-scale text processing.
 4. Semantic Awareness
- spaCy supports word vectors and similarity comparisons, enabling semantic search and clustering.


2. Comparative Analysis

Compare Scikit-learn and TensorFlow in terms of:

Target applications (e.g., classical ML vs. deep learning).
-Scikit-learn is ideal for traditional ML tasks like fraud detection or customer segmentation. TensorFlow excels in tasks requiring deep learning, such as autonomous driving or voice recognition.


Ease of use for beginners.
-Scikit-learn is often recommended as a first ML library due to its simplicity. TensorFlow offers more power but demands deeper understanding, especially when building custom models.

Community support.
-Both libraries have vibrant communities, but TensorFlow benefits from Google’s backing and a broader ecosystem for deployment and scaling.

PART 3: ETHICS & OPTIMIZATION (10%)
1. Ethical Considerations

Identify potential biases in your MNIST or Amazon Reviews model. How could tools like TensorFlow Fairness Indicators or spaCy’s rule-based systems mitigate these biases?
 Potential Biases
 MNIST Model
MNIST consists of handwritten digits, and its biases typically stem from:
- Sampling bias: Digits may be more representative of certain age groups or writing styles.
- Style sensitivity: If the model struggles with slanted or messy handwriting, it may unfairly penalize some users.
- Device differences: Input images from newer devices might differ in resolution or contrast.
   Amazon Reviews Model
This model works with natural language and carries more nuanced risks:
- Sentiment bias: The model might associate certain words with positive/negative sentiment unfairly due to skewed training data.
- Demographic bias: Language patterns from different regions, dialects, or cultures may not be equally represented.
- Topic bias: Reviews in certain product categories (e.g. tech vs. beauty) may be overrepresented, influenci

 Mitigation Tools
1. TensorFlow Fairness Indicators
Ideal for models like Amazon Reviews that work with structured outputs:
- Provides sliced evaluation by group (e.g., gender or dialect).
- Highlights performance disparities in metrics like precision and recall.
- Integrates easily into TensorFlow pipelines for automated fairness monitoring.
   Example: You could segment reviews by reviewer location and detect if accuracy drops significantly for one region—pinpointing demographic bias.
2. spaCy’s Rule-Based Systems
While not a fairness tool per se, it helps mitigate bias in language preprocessing:
- Allows crafting custom tokenization rules, reducing misinterpretation of dialects or idioms.
- Enables detection and normalization of identity-related terms to prevent their over-weighting.
- Helps annotate data more precisely, supporting fairer training and evaluation.
   Example: If your review model misinterprets informal Kenyan slang, spaCy rules could help normalize it without losing nuance.
