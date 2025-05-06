# SEEM3650 Practical Exam 2 babychatgpt 
nanoGPT
Descripe: Explore training GPT models using the nanoGPT repository. While
training functioning GPT models typically requires multiple GPUs, we will work with a much smaller
version, referred to as BabyGPT. This can be trained on a CPU, though using a GPU (e.g., via Google
Colab) is recommended for faster results.
SID:1155193525
Name: Leung ShingYip

# Practical Exam Report
##  Step 1 : Cloning

!git clone https://github.com/karpathy/nanoGPT

Given:Cloning into 'nanoGPT'...
remote: Enumerating objects: 686, done.
remote: Total 686 (delta 0), reused 0 (delta 0), pack-reused 686 (from 1)
Receiving objects: 100% (686/686), 954.03 KiB | 23.85 MiB/s, done.
Resolving deltas: 100% (387/387), done.

## Step 2: Shakespeare Model Output
## Shakespeare Character-level Model Samples

Overriding: out_dir = out-shakespeare-char
Overriding: max_new_tokens = 1000
number of parameters: 10.65M
Loading meta from data/shakespeare_char/meta.pkl...


**First 5 lines outputs:**
AUTOLYCUs: O, will you be straightMENENlUS: Stirrd your gates?
CORIOLANUS: You met?MENENlUs: Nay, no more not to be much:lf you find it out of much but soils, since l lay you, i'l speak with her person of else no moreAUFiDlUs: l would have show'd your name. Be patient o'er the world that Would so what evil so you would have no precise of mine; Which
you have forgot a sign of sheet in all of person The ground.

## Step 3: Structure Exploration validation loss vs layer depth

The result of step 3
Due to the laptop construction and colab have to pay to get gpu thus i use cpu and the loss at iteration down from 5000 to 50 
# Validation Loss vs. Number of Layers (n_head=5)

- X-axis: Number of Layers [2, 3, 5, 7]
- Y-axis: Validation Loss at Iteration 50 [1.50, 1.44, 1.45, 1.46]
- Plot Type: Line plot with circle markers
- Title: Validation Loss vs. Number of Layers (n_head=5)
- X-label: Number of Layers
- Y-label: Validation Loss at Iteration 50
- Grid: Enabled
- Saved as: figures/loss_vs_layers.png

Description:
- The plot shows a line connecting four points corresponding to n_layer={2, 3, 5, 7} with n_head=5.
- The validation loss starts at 1.50 (n_layer=2), dips to a minimum of 1.44 (n_layer=3), slightly rises to 1.45 (n_layer=5), and then to 1.46 (n_layer=7).
- The trend suggests that n_layer=3 achieves the lowest validation loss, while deeper layers (n_layer=7) slightly increase the loss.

The graph may take a look at generate loss vs layers .png

## Step 4 code generation:
**20 lines**
import spacy
from spacy.lang.en import English
from spacy.tokens import Doc

def initialize_nlp():
    return English()

class TextProcessor:
    def __init__(self, nlp):
        self.nlp = nlp

    def process(self, text):
        doc = self.nlp(text)
        return [token.text for token in doc]

def validate_input(text):
    if not text or not isinstance(text, str):
        raise ValueError("Input must be a non-empty string")
    return text

if __name__ == "__main__":
    nlp = initialize_nlp()
    processor = TextProcessor(nlp)
    text = "This is a test sentence for processing."
    tokens = processor.process(text)
    print(tokens)







