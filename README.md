**Sentiment-Aware Chatbot with Hugging Face & Gradio**

## Project Overview

This project demonstrates a sentiment-aware chatbot capable of analyzing user input and adjusting its responses based on the detected sentiment. By leveraging **Hugging Face's transformers** and **Gradio**, this chatbot not only generates conversational responses but also tailors those responses based on whether the user is expressing positive, negative, or neutral sentiment.

The core functionality revolves around **sentiment analysis** using pre-trained models from Hugging Face, combined with a **CSV-based response system** to store and manage different replies for each sentiment category. The project also features a user-friendly interface powered by **Gradio**, allowing real-time interaction with the chatbot through a web browser.

## Features

- **Sentiment Analysis**: The chatbot uses Hugging Face's `pipeline('sentiment-analysis')` to detect the sentiment of user input (Positive, Negative, or Neutral).
- **Custom Responses Based on Sentiment**: A CSV file stores various responses mapped to different sentiment categories, allowing for dynamic and contextually appropriate replies.
- **Gradio Web Interface**: The project uses Gradio to create a simple, interactive web interface that users can access and engage with in real-time.
- **Real-time Sentiment-Adapted Responses**: Based on the detected sentiment, the chatbot adapts its response to offer more empathetic or encouraging replies.

## Tools & Libraries Used

1. **Hugging Face Transformers**: Used for sentiment analysis. The chatbot uses a pre-trained model to classify user input into positive, negative, or neutral sentiment.
   - Model: `distilbert-base-uncased-finetuned-sst-2-english` for faster performance.
   - Hugging Face pipeline: `sentiment-analysis`.

2. **Gradio**: Provides a user-friendly interface for interaction with the chatbot. Gradio allows the chatbot to be easily deployed and accessed in a web browser.

3. **CSV for Response Management**: The chatbot pulls its responses from a CSV file, where each row contains a response mapped to a sentiment type. This allows for flexible and dynamic responses.

4. **Google Colab or Local Environment**: The project can be run in a local Python environment or in Google Colab for ease of setup. Colab also offers free GPU support, which speeds up the model inference.

## Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo/sentiment-chatbot.git
   cd sentiment-chatbot
   ```

2. **Install the necessary dependencies**:
   This project requires the following Python libraries:
   - `transformers`
   - `gradio`
   You can install them using pip:
   ```bash
   pip install transformers gradio
   ```

3. **Ensure the `responses.csv` file is present**:
   The `responses.csv` file stores chatbot replies based on sentiment. You can create or modify this file to adjust responses for each sentiment category (Positive, Negative, Neutral).

4. **Run the chatbot**:
   You can start the chatbot by running the script in your environment:
   ```bash
   python app.py
   ```

5. **Run in Google Colab **:
   If you're using Google Colab, make sure to enable GPU for faster inference. You can set this in **Runtime** > **Change runtime type** and choose **GPU**.

6. **Access the Web Interface**:
   Once the chatbot starts, a Gradio interface will be launched, and you can access the chatbot through the provided URL in your browser. The chatbot will analyze your inputs and respond based on the detected sentiment.

## How It Works

1. **Sentiment Detection**: When the user inputs text, the chatbot first passes it through a Hugging Face sentiment analysis pipeline to determine whether the sentiment is positive, negative, or neutral.
   
2. **Response Generation**: Based on the detected sentiment, the chatbot retrieves an appropriate response from the pre-defined CSV file.

3. **Gradio Interface**: The interaction with the chatbot happens through Gradio's web interface, where users can input text and receive instant responses.

## Example Use Cases

- **Customer Support Chatbot**: Detects frustration or satisfaction and provides responses tailored to calming or encouraging the user.
- **Mental Health Assistant**: Identifies negative sentiments and offers uplifting messages to provide emotional support.
- **Educational Tutor**: Adjusts explanations based on user sentiment, offering additional help when detecting frustration.


## Contribution

Feel free to contribute to this project by submitting pull requests, reporting issues, or suggesting features. All contributions are welcome!

---
