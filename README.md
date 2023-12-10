# Experiential_Learning_Tartan_Coach
This is the GitHub repository of Tartan Coach chatbot - which is a specialized chatbot for mental health
# README for Chatbot with PALM API Integration

This repository contains a Python script for a chatbot that integrates with the PALM (Predictive AI Language Model) API to provide mental health advice and support to users. The chatbot is designed to have conversations with users, offer guidance on mental health-related topics, and store user interactions and feedback in a SQLite database.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Database Configuration](#database-configuration)
- [Feedback and User Sessions](#feedback-and-user-sessions)
- [Email Notifications](#email-notifications)
- [Customizing the Chatbot](#customizing-the-chatbot)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This chatbot leverages the PALM API for generating text responses and provides mental health support by engaging in conversations with users. It can be used as a foundation for building a mental health chatbot or for educational purposes.

Key functionalities include:
- Integration with the PALM API for generating text responses.
- SQLite database for storing user interactions, feedback, and session data.
- Email notifications to a specified recipient at the end of a conversation.
- Customizable mental health advice responses based on user input.

## Features

- Interaction with users via a text-based interface.
- Real-time generation of mental health advice using the PALM API.
- Storage of user interactions and feedback in a SQLite database.
- Email notifications with conversation summaries (optional).
- Basic natural language processing for identifying mental health-related queries.

## Requirements

Before using the chatbot, ensure that you have the following requirements installed:

- Python 3.x
- Required Python packages (install using `pip install [package-name]`):
  - requests
  - sqlite3
  - pandas
  - google.generativeai (PALM API integration)
  - nltk
  - smtplib
  - email.mime (for sending emails)
  - rake-nltk (for keyword extraction)

You will also need a valid API key from the PALM API to use the PALM text generation service.

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/yourproject.git
   cd yourproject
   ```

2. Install the required Python packages using pip:

   ```bash
   pip install requests sqlite3 pandas generativeai nltk smtplib rake-nltk
   ```

3. Update the `API_KEY` variable in the code with your valid PALM API key.

## Usage

To run the chatbot, execute the Python script from your terminal:

```bash
python chatbot.py
```

The chatbot will initiate a conversation with the user, provide mental health advice, and store interactions in the database. It will ask for feedback and an email address at the end (optional) to send a conversation summary.

## Database Configuration

The chatbot uses an SQLite database to store user interactions and feedback. The database is created and configured within the code. The default database file name is 'chatbot_feedback_v3.db'. You can customize this by modifying the `DB_NAME` variable in the code.

## Feedback and User Sessions

User interactions and feedback are stored in the database. The tables used for storing data include:
- `feedback`: Stores user input, chatbot responses, feedback, and email addresses.
- `user_sessions`: Logs user sessions and input.
- `users`: Keeps track of registered users.

You can access and query this data for analysis and improvement of the chatbot.

## Email Notifications

The chatbot can send email notifications with conversation summaries to a specified recipient at the end of a conversation. To enable this feature, provide an email address when prompted during the conversation.

The email functionality is configured to use the SMTP server for Outlook. You may need to adjust the SMTP settings and sender information if you want to use a different email service.

## Customizing the Chatbot

You can customize the chatbot's behavior and responses by modifying the code. Some potential areas for customization include:
- Adjusting the keywords for identifying mental health-related queries.
- Enhancing the logic for generating mental health advice based on user input.
- Customizing the email content and notification settings.
- Implementing more advanced natural language processing techniques.

## Contributing

Contributions to this project are welcome! If you have ideas for improvements or would like to add new features, please feel free to submit pull requests or open issues on the GitHub repository.

---

Thank you for using the Mental Health Chatbot with PALM API Integration! If you have any questions or encounter issues, please don't hesitate to reach out and seek support.
