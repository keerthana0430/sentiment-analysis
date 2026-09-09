# sentiment-analysis
Sentiment Analysis using Hugging Face and Streamlit
A simple web-based Sentiment Analysis application that uses a pre-trained Hugging Face Transformer model to identify whether a given sentence expresses a Positive or Negative sentiment.

The application provides the predicted sentiment along with the model's confidence score through an interactive Streamlit interface.

Project Overview
This project demonstrates how Natural Language Processing (NLP) and Transformer-based models can be integrated into a lightweight web application.

The user enters a sentence into the application. The text is then passed to a pre-trained sentiment-analysis model from Hugging Face. The model analyzes the text and returns:

Sentiment label: Positive or Negative
Confidence score of the prediction
The result is displayed immediately through the Streamlit interface.

Key Features
Interactive web interface using Streamlit
Pre-trained Transformer model from Hugging Face
Positive and Negative sentiment classification
Confidence score displayed as a percentage
Input validation for empty text
Model caching using Streamlit's st.cache_resource
No model training required
Simple and lightweight NLP application
Technologies and Tools
Technology / Tool	Purpose
Python	Core programming language
Streamlit	Creates the interactive web application
Hugging Face Transformers	Provides the pre-trained NLP model
DistilBERT	Performs sentiment classification
PyTorch	Backend used by the Transformer pipeline
VS Code	Development environment
Git & GitHub	Version control and project hosting
AI Model
This project uses:

Model: distilbert-base-uncased-finetuned-sst-2-english

This is a fine-tuned DistilBERT model designed for sentiment classification using the Stanford Sentiment Treebank (SST-2) dataset.

The model predicts two classes:

POSITIVE
NEGATIVE
The model also returns a confidence score representing how confident it is in the prediction.

How the Application Works
The application follows a simple NLP workflow:

User enters a sentence
          |
          v
   Streamlit Interface
          |
          v
     Text Validation
          |
          v
 Hugging Face Pipeline
          |
          v
    DistilBERT Model
          |
          v
 Sentiment Prediction
          |
          v
 Positive / Negative
          |
          v
 Confidence Score
          |
          v
   Result displayed
Workflow Explanation
1. User Input

The user enters a sentence into the Streamlit text area.

2. Input Validation

The application checks whether the user has entered any text.

If the input is empty, a warning message is displayed.

3. Model Processing

The input text is passed to the Hugging Face sentiment-analysis pipeline.

4. Sentiment Classification

The DistilBERT model analyzes the sentence and predicts either Positive or Negative sentiment.

5. Confidence Calculation

The model provides a confidence score for its prediction.

6. Result Display

Streamlit displays the predicted sentiment and confidence percentage on the web interface.
<img width="685" height="329" alt="image" src="https://github.com/user-attachments/assets/def1d05c-abd7-442d-8b48-1044f2922ebd" />

Important Functions Used
st.set_page_config()
Configures the Streamlit page, including:

Page title
Page icon
Browser tab settings
st.set_page_config(
    page_title="Sentiment Analysis",
    page_icon="..."
)
st.title()
Displays the main title of the application.

st.text_area()
Provides a text box where users can enter sentences for analysis.

st.button()
Creates the Analyze Sentiment button that starts the prediction process.

st.cache_resource
Caches the loaded AI model so that Streamlit does not reload the model every time the application changes or the user interacts with it.

This improves application performance.

pipeline()
The Hugging Face pipeline() function provides a simple interface for performing sentiment analysis using a pre-trained Transformer model.

pipeline(
    "sentiment-analysis",
    model="distilbert-base-uncased-finetuned-sst-2-english"
)
sentiment_model(text)
Sends the user's text to the trained model and receives the prediction.

st.success() and st.error()
These functions display different result messages depending on whether the sentiment is Positive or Negative.

Project Structure
sentiment-analysis/
│
├── app.py
├── requirements.txt
└── README.md
Files
app.py

Contains the complete Streamlit application, model loading, input handling, prediction logic, and result display.

requirements.txt

Contains the Python dependencies required to run the project.

README.md

Provides project documentation and setup instructions.

Installation
1. Clone the Repository
git clone https://github.com/your-username/sentiment-analysis.git
2. Open the Project Folder
cd sentiment-analysis
3. Install Dependencies
pip install -r requirements.txt
4. Run the Application
streamlit run app.py
Streamlit will start the application and provide a local URL in the terminal.

Example
Input
I really enjoyed this movie!
Output
Sentiment: POSITIVE
Confidence: 99.XX%
Another example:

The service was extremely disappointing.
Output:

Sentiment: NEGATIVE
Confidence: XX.XX%
<img width="886" height="770" alt="image" src="https://github.com/user-attachments/assets/74565e9a-57b7-4675-9cd3-fed339908b6e" />

Limitations
The model only predicts Positive and Negative sentiment.
It may not correctly understand sarcasm or highly ambiguous statements.
Prediction accuracy can vary depending on the wording and context of the input.
The model is specifically fine-tuned for English sentiment classification.
Future Improvements
Possible improvements include:

Add Neutral sentiment classification
Support multiple languages
Analyze multiple sentences or documents
Add sentiment history
Visualize sentiment confidence
Add batch CSV sentiment analysis
Deploy the application online
Add charts for sentiment statistics
Improve the user interface
Add an API layer for external applications
Learning Outcomes
Through this project, the following concepts are demonstrated:

Natural Language Processing
Transformer-based NLP models
Hugging Face Transformers
Pre-trained AI models
Streamlit application development
Model inference
Confidence scores
Python application development
Git and GitHub project management
Conclusion
This project demonstrates how a pre-trained Transformer model can be integrated with Streamlit to create a practical NLP application.

Instead of training a machine-learning model from scratch, the application uses an existing fine-tuned DistilBERT model and focuses on model inference, user interaction, and result visualization.

