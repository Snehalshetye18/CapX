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

### 2. Create a Telegram Developer account and obtain the API keys:
- Go to [Telegram API development tools](https://my.telegram.org/auth) to create a new application.
- Obtain your `api_id` and `api_hash` after creating the application.

### 3. Replace the placeholders in `Telegram for CapX.ipynb`:
In the `Telegram for CapX.ipynb` file, replace the placeholders with your Telegram API credentials:
```python
api_id = 'your_api_id'  # Replace with your API ID
api_hash = 'your_api_hash'  # Replace with your API Hash
target_channel = 'channel_username'  # Replace with the target Telegram channel username
