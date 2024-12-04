# CapX
# Telegram Stock Prediction Project

This project scrapes messages from Telegram channels focused on stock predictions, performs sentiment analysis on the scraped data, and builds a machine learning model to predict stock movements based on sentiment and message content.

## Prerequisites

- Python 3.x (Recommended: Python 3.8 or higher)
- Telegram Developer Account (for accessing the Telegram API)
- Basic understanding of Python, Machine Learning, and Natural Language Processing (NLP)

## Setup

Follow these steps to set up and run the project:

### 1. Install dependencies:
Clone the repository and install the required dependencies by running:
    ```bash
    pip install -r requirements.txt
    ```

### 2. Create a Telegram Developer Account and Obtain API Credentials:
To access the Telegram API, you'll need to create a Telegram Developer account and generate an API ID and API Hash.

#### Steps to create a Telegram Developer account:
1. **Create a Telegram Account** (if you don't already have one):
    - Download the [Telegram app](https://telegram.org/) and sign up for an account.

2. **Go to the Telegram API Development Tools page**:
    - Open [Telegram API Development Tools](https://my.telegram.org/auth) in your browser.
  
3. **Log in** with your Telegram account credentials.

4. **Create a new application**:
    - Click on the "Create new application" button.
    - Fill in the required fields such as "App title," "Short name," etc.
    - You can leave "URL" as blank or provide a website URL if you have one.
    - Select the platform (you can choose "Other" if it's not listed).
  
5. **Obtain the API credentials**:
    - After creating the application, you will be shown your **API ID** and **API Hash**.
    - Copy these credentials as you will need to use them in the project.

6. **Add the credentials to the code**:
    - Replace the following placeholders in `scraper.py` with your Telegram API credentials:
      ```python
      api_id = 'your_api_id'  # Replace with your API ID
      api_hash = 'your_api_hash'  # Replace with your API Hash
      target_channel = 'channel_username'  # Replace with the target Telegram channel username
      ```

### 3. Running the Scraper to Collect Data:
Once you've configured your Telegram API credentials, you can run the scraper to collect messages from the selected Telegram channel(s).

#### Steps to run the scraper:
1. Open a terminal or command prompt.
2. Navigate to the project directory where `Telegram for CapX.ipynb` is located.
3. Run the following command to start the scraper:
    ```bash
    jupyter execute Telegram for CapX.ipynb
    ```

The scraper will connect to the Telegram API, fetch the messages from the specified channel, and save the scraped data in a CSV file (`telegram_data.csv`).

---

### 4. Sentiment Analysis and Data Analysis:
- The `notebooks/Telegram for CapX.ipynb` Jupyter notebook is used to perform sentiment analysis on the scraped messages. It uses NLP techniques to classify the sentiment of each message into categories: positive, negative, or neutral.

#### Steps to run sentiment analysis:
1. Open the `Telegram for CapX.ipynb` notebook in Jupyter.
2. Run the cells to analyze the sentiment of the messages.
3. The sentiment scores (positive, negative, neutral) will be saved in the CSV file alongside the messages.

---

### 5. Model Training:
- The `Telegram for CapX.ipynb` script takes the sentiment data and trains a machine learning model to predict stock movements.

#### Steps to train the model:
1. Open a terminal or command prompt.
2. Navigate to the project directory where `Telegram for CapX.ipynb` is located.
3. Run the following command to train the machine learning model:
    ```bash
    jupyter execute Telegram for CapX.ipynb
    ```

This script will load the sentiment data from `telegram_data.csv`, preprocess it, and train the machine learning model using algorithms like Logistic Regression, Random Forest, etc.

---

## Files

- **`telegram_data.csv`**: This CSV file contains the scraped messages from the selected Telegram channel(s), including columns for the date, sender ID, message text, and sentiment polarity score.
- **`Telegram for CapX.ipynb`**: Python script that connects to the Telegram API using `Telethon` and scrapes messages from a target Telegram channel.
- **`Telegram for CapX.ipynb`**: Python script that trains a machine learning model for stock movement prediction based on the sentiment of the messages.
- **`notebooks/Telegram for CapX.ipynb`**: Jupyter notebook for performing sentiment analysis on the scraped data.

---
