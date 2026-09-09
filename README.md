# Sentiment Analysis using Streamlit & Hugging Face

## Project Overview

This project is a simple and interactive **Sentiment Analysis Web Application** built using **Python, Streamlit, and Hugging Face Transformers**.

The application analyzes a given sentence and determines whether the sentiment expressed in the text is **Positive** or **Negative**. It also displays the confidence score of the prediction.

This project demonstrates how Natural Language Processing (NLP) and pre-trained Transformer models can be integrated into a user-friendly web application.

---

## Project Objective

The main objective of this project is to create a simple web application that can automatically identify the sentiment of a given piece of text.

The application can be used to understand whether a sentence expresses:

* Positive Sentiment
* Negative Sentiment

Along with the sentiment, the application also provides the **confidence percentage** of the prediction.

---

## Features

* AI-powered sentiment analysis
* User-friendly text input area
* Positive sentiment detection
* Negative sentiment detection
* Confidence score display
* Fast prediction using a pre-trained Hugging Face model
* Interactive web interface using Streamlit
* Simple and beginner-friendly implementation
* Efficient model loading using Streamlit caching

---

## Technologies Used

### Python

Python is used as the main programming language for developing the application.

### Streamlit

Streamlit is used to create the interactive web interface without requiring HTML, CSS, or JavaScript.

### Hugging Face Transformers

The Hugging Face Transformers library is used to load and run the pre-trained sentiment analysis model.

### DistilBERT

The project uses the following pre-trained model:

`distilbert-base-uncased-finetuned-sst-2-english`

This model is a fine-tuned DistilBERT model designed for English sentiment classification.

---

## How the Project Works

The application follows these basic steps:

1. The user opens the Streamlit application.
2. The user enters a sentence in the text area.
3. The user clicks the **Analyze Sentiment** button.
4. The Hugging Face sentiment analysis pipeline processes the text.
5. The model predicts the sentiment.
6. The application displays the sentiment label and confidence score.
7. A positive or negative message is displayed based on the prediction.

---

## Project Structure

```text
Sentiment-Analysis/
│
├── app.py
├── README.md
└── requirements.txt
```

---

## Required Libraries

The project requires the following Python libraries:

```text
streamlit
transformers
torch
```

You can install the required packages using:

```bash
pip install streamlit transformers torch
```

---

## How to Run the Project

### Step 1: Clone the Repository

Clone the GitHub repository to your computer.

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### Step 2: Open the Project Folder

```bash
cd Sentiment-Analysis
```

### Step 3: Install Dependencies

Run:

```bash
pip install streamlit transformers torch
```

### Step 4: Run the Streamlit Application

Run the following command:

```bash
streamlit run app.py
```

### Step 5: Open the Application

After running the command, Streamlit will provide a local URL.

Usually, it will look like:

```text
http://localhost:8501
```

Open this URL in your web browser to access the application.

---

## Example

### Input

```text
I really enjoyed this movie!
```

### Output

```text
Positive Sentiment

Sentiment: POSITIVE
Confidence: 99.XX%
```

---

### Another Example

### Input

```text
I did not like this product.
```

### Output

```text
Negative Sentiment

Sentiment: NEGATIVE
Confidence: XX.XX%
```

---

## Model Information

This project uses the following pre-trained model:

**Model:** `distilbert-base-uncased-finetuned-sst-2-english`

The model is based on **DistilBERT**, a smaller and faster version of BERT. It has been fine-tuned for sentiment classification using the **SST-2 (Stanford Sentiment Treebank)** dataset.

The model classifies English text into two categories:

* `POSITIVE`
* `NEGATIVE`

The model also provides a confidence score for its prediction.

---

## Confidence Score

The confidence score represents how confident the model is about its prediction.

For example:

```text
Sentiment: POSITIVE
Confidence: 98.50%
```

This means the model is approximately **98.50% confident** that the given sentence expresses a positive sentiment.

---

## User Interface

The application provides a simple interface containing:

* Project title
* Project description
* Text input area
* Analyze Sentiment button
* Result section
* Sentiment classification
* Confidence percentage

The interface is designed to be simple and easy to use.

---

## Future Enhancements

The project can be improved in the future by adding:

* Sentiment analysis charts
* Positive and negative probability graphs
* Analysis of multiple sentences
* CSV file upload
* Chat-style sentiment analysis
* Support for multiple languages
* Improved responsive user interface
* Sentiment analysis history
* Downloadable analysis reports

---

## Limitations

* The current model is mainly designed for English text.
* It classifies the input into only positive or negative sentiment.
* Sarcasm and complex expressions may not always be classified correctly.
* The prediction depends on the quality and context of the input text.
* The first model loading may take some time because the pre-trained model needs to be downloaded.

---

## Learning Outcomes

By completing this project, the following concepts can be learned:

* Basics of Natural Language Processing
* Sentiment Analysis
* Using Hugging Face Transformers
* Working with pre-trained AI models
* Creating web applications using Streamlit
* Using Python libraries for AI applications
* Handling user input
* Displaying AI prediction results
* Understanding model confidence scores

---

## Conclusion

The **Sentiment Analysis using Streamlit & Hugging Face** project demonstrates how a pre-trained Natural Language Processing model can be integrated into a simple web application.

The project provides an easy way for users to enter text and receive an AI-generated sentiment prediction along with its confidence score.

This project is suitable for beginners who are interested in learning about **Python, Artificial Intelligence, Natural Language Processing, Hugging Face, and Streamlit**.

---

## Author

**Keerthana**

B.Sc. Computer Science with Artificial Intelligence

