# Lambeq-library
```markdown
# QNLP_Assignment.ipynb



### Overview

This Jupyter Notebook explores Quantum Natural Language Processing using the lambeq library, PyTorch, and PennyLane. The QNLP journey involves several key stages, starting with data input and preprocessing. Sentences undergo a transformative journey, evolving into intricate string diagrams, simplification, and ultimately becoming quantum circuits through the IQPAnsatz method.

At the pinnacle of this innovation lies the XORSentenceModel, a hybrid QNLP marvel. This model seamlessly combines quantum circuits with a neural network to discern the thematic relevance between pairs of sentences.

### Architecture

The architecture of the QNLP model undergoes a meticulous shaping process, intricately molded by the grammatical composition of the input sentence. Lambeq plays a crucial role, orchestrating the symphony with its adept parsing mechanism. In its latest rendition, lambeq proudly introduces Bobcat, a neural network-driven parser of remarkable sophistication, while also broadening its horizons by harmonizing with an array of other parsers.

As the parsing phase gracefully concludes, lambeq crafts a syntax tree for the sentence, a masterpiece that seamlessly metamorphoses into an abstract entity known as a "string diagram." This intricate representation gracefully encapsulates the intricate web of linguistic relationships concealed within the sentence's tapestry. Remarkably, this transformative step operates independently of the nitty-gritty technical details, ensuring its seamless integration into the intricate fabric of training procedures.

### PennyLaneModel

To illustrate this multifaceted process, we introduce the debut of a hybrid marvel, aptly named PennyLaneModel. The very essence of this model's existence is to embark on the noble quest of discerning whether a given pair of sentences intertwines with divergent themes. To attain this lofty goal, we enlist the formidable might of the IQPAnsatz, a versatile tool adept at transmuting string diagrams into intricate quantum circuits. It's noteworthy that these circuits gracefully transition into the realm of PennyLane, undergoing an automated metamorphosis as they are entrusted to the model's discerning intelligence.

### Installation

To run this notebook, make sure to install the required libraries using the following command:

```bash
!pip install lambeq
```

### Usage

```python
from lambeq import SpacyTokeniser

# Tokenize a sentence
tokeniser = SpacyTokeniser()
sentence = "We have a very small semester this time"
tokens = tokeniser.tokenise_sentence(sentence)
print(tokens)

# Parse and draw a string diagram
from lambeq import BobcatParser, pregroups

parser = BobcatParser(verbose='suppress')
diagram = parser.sentence2diagram(tokens, tokenised=True)
pregroups.draw(diagram, figsize=(23, 4), fontsize=12)
```

Feel free to explore and experiment with the provided code to deepen your understanding of Quantum Natural Language Processing!

