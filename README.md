# Soft Nexis Internship: Project-3-Natural-Language-Processing
**TF-IDF and Applications of Sentiment Analysis**

TF-IDF (Term Frequency–Inverse Document Frequency) is a technique used in Natural Language Processing (NLP) to determine how important a word is within a document compared to a collection of documents. It helps computers identify the most meaningful words while reducing the importance of very common words such as "the," "is," and "and."

TF-IDF consists of two parts. The first part, Term Frequency (TF), measures how often a word appears in a document. Words that appear more frequently receive higher TF values. The second part, Inverse Document Frequency (IDF), measures how unique a word is across all documents. If a word appears in many documents, its IDF value becomes lower because it is less useful for distinguishing one document from another. By multiplying TF and IDF, TF-IDF assigns a score to each word, highlighting words that are frequent in a particular document but uncommon across the entire dataset.

TF-IDF is widely used in search engines, document classification, keyword extraction, and recommendation systems because it helps identify the most relevant information in large amounts of text.

Sentiment analysis is another important NLP technique that determines whether a piece of text expresses a positive, negative, or neutral opinion. It has many practical applications in the real world.

One application is customer feedback analysis. Companies collect reviews, survey responses, and social media comments from customers. Sentiment analysis automatically identifies customer satisfaction levels and helps businesses understand what customers like or dislike about their products and services.

Another application is social media monitoring. Organizations, brands, and political groups analyze public opinions expressed on platforms such as Twitter, Facebook, and Instagram. Sentiment analysis helps them track public reactions to events, products, advertisements, or campaigns in real time and make informed decisions based on public sentiment.

In conclusion, TF-IDF helps identify important words in text data, while sentiment analysis helps understand people's opinions and emotions. Both techniques play a significant role in modern Natural Language Processing applications.

**ENVIRONMENT SETUP**

## Step 1: Check Python Installation

Open **Command Prompt** and run:

```bash
python --version
```

or

```bash
py --version
```

You should see something like:

```text
Python 3.12.5
```

If not, install Python from:

[Python Official Website](https://www.python.org/downloads/?utm_source=chatgpt.com)

During installation, make sure **"Add Python to PATH"** is checked.

---

## Step 2: Create a Project Folder

Create a folder:

```text
NLP_Sentiment_Analysis
```

Open this folder in VS Code.

---

## Step 3: Open Terminal in VS Code

Press:

```text
Ctrl + `
```

or go to:

```text
Terminal → New Terminal
```

---

## Step 4: Create a Virtual Environment (Recommended)

Run:

```bash
python -m venv venv
```

Activate it:

### Windows

```bash
venv\Scripts\activate
```

You should see:

```text
(venv) C:\Users\...
```

---

## Step 5: Install Required Libraries

Run:

```bash
pip install nltk scikit-learn pandas matplotlib seaborn wordcloud jupyter notebook ipykernel
```

Verify installation:

```bash
pip list
```

You should see packages such as:

```text
nltk
pandas
scikit-learn
matplotlib
seaborn
wordcloud
jupyter
```

---

## Step 6: Create a Jupyter Notebook

In VS Code:

1. Click **New File**
2. Save as:

```text
sentiment_analysis.ipynb
```

or

```text
project3.ipynb
```

---

## Step 7: Download NLTK Data

Paste this into the first notebook cell and run it:

```python
import nltk

nltk.download('stopwords')
nltk.download('punkt')
nltk.download('punkt_tab')      # Needed for newer NLTK versions
nltk.download('wordnet')
nltk.download('omw-1.4')

print("All NLTK data downloaded successfully!")
```

Expected output:

```text
All NLTK data downloaded successfully!
```

---

## Step 8: Test All Libraries

Create a new cell and run:

```python
import pandas as pd
import nltk
import sklearn
import matplotlib.pyplot as plt
import seaborn as sns
from wordcloud import WordCloud

print("Everything installed correctly!")
```

Expected output:

```text
Everything installed correctly!
```

---

## Step 9: Load the Sample Dataset

Run:

```python
import pandas as pd

reviews = [
    ('This movie was absolutely fantastic! Best film of the year.', 'positive'),
    ('Terrible acting and boring plot. Complete waste of time!', 'negative'),
    ('Loved every minute of it. The director did an amazing job.', 'positive'),
    ('Awful storyline. I fell asleep halfway through.', 'negative'),
    ('Brilliant performances! The cinematography was breathtaking.', 'positive'),
    ('Worst movie I have ever seen. Do not waste your money.', 'negative'),
    ('Heartwarming and beautifully crafted. A true masterpiece.', 'positive'),
    ('Dull and predictable. The script was painfully bad.', 'negative')
]

df = pd.DataFrame(reviews, columns=['review', 'sentiment'])

print("Dataset Shape:", df.shape)
df.head()
```

Expected output:

```text
Dataset Shape: (8, 2)
```

---

## If you get errors

### Error: `No module named nltk`

Run:

```bash
pip install nltk
```

### Error: `No module named wordcloud`

Run:

```bash
pip install wordcloud
```

### Error: `Resource punkt_tab not found`

Run:

```python
import nltk
nltk.download('punkt_tab')
```

### Error: `Select Kernel`

Press **Select Kernel** in the top-right of the notebook and choose:

```text
Python (venv)
```
