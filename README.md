# workout-calendar
An app to pull workout data from Google Calendar and analyze using OpenAI API.

⸻

Google Calendar Workout Analytics

Google Calendar Workout Analytics is a tool that extracts workout data from your Google Calendar and leverages OpenAI’s API to provide detailed fitness analysis. The project is implemented as a Google Colab Notebook divided into three main sections: configuration & authentication, Google Calendar data extraction, and fitness data analysis with OpenAI.

Features
	•	Google Calendar Integration:
Fetches events from your calendar, allowing you to log workouts in a non-paywalled, free, and universal manner.
	•	Fitness Data Analysis:
Uses OpenAI’s GPT models to classify workouts (e.g., weightlifting vs. triathlon training), parse exercise details (sets, reps, weights), and offer insights on your fitness data.
	•	Modular & Secure:
The code is organized into clear sections with helper functions to reduce redundancy. Sensitive information like API keys and email addresses are replaced with placeholders.
	•	Easy Setup:
Step-by-step instructions guide you through setting up your Google Cloud project, enabling the Calendar API, configuring authentication, and integrating with OpenAI.

Getting Started

Prerequisites
	•	A Google Cloud project with the Calendar API enabled.
	•	A service account with a JSON key for accessing the Calendar API.
	•	Your Google Calendar shared with the service account (if needed).
	•	An OpenAI API key (set up securely via environment variables or a secure configuration file).
	•	Google Colab (recommended for running the notebook).

Setup Instructions
	1.	Google Cloud Console Setup:
	•	Project & API:
Create or select a project in the Google Cloud Console and enable the Google Calendar API.
	•	Service Account:
Create a service account under IAM & Admin → Service Accounts and download the JSON credentials file.
Important: Keep this credentials file secure and do not commit it to public repositories.
	•	Calendar Sharing:
Share your calendar with the service account’s email address, granting appropriate permissions.
	2.	OpenAI API Key:
	•	Obtain your OpenAI API key from the OpenAI platform.
	•	Securely set your API key, for example as an environment variable named OPENAI_API_KEY.

Running the Notebook
	1.	Open the notebook in Google Colab.
	2.	Install the required packages by running:

!pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib openai


	3.	When prompted, upload your service account credentials JSON file.
	4.	Replace placeholder values in the notebook:
	•	Update "YOUR_CALENDAR_ID" with your actual calendar ID.
	•	Ensure "YOUR_OPENAI_API_KEY" is set securely.
	5.	Execute the notebook cells sequentially:
	•	Section 1: Configuration & Authentication – handles credential upload and user authentication.
	•	Section 2: Google Calendar Data Extraction – builds the API service and retrieves events.
	•	Section 3: Integration with OpenAI – sends your workout data for analysis.

Project Structure

The notebook is organized into three main sections:
	•	Configuration & Authentication:
Contains helper functions (upload_credentials() and authenticate_and_load_creds()) to handle file uploads and authentication with Google Cloud.
	•	Google Calendar Data Extraction:
Sets up the Calendar API service and retrieves upcoming events from your calendar. Replace the placeholder calendar ID with your own.
	•	OpenAI Fitness Data Analysis:
Uses OpenAI’s API to analyze and classify workout data. This section outputs a JSON summary along with insights and patterns from your workout sessions.

Contributing

Contributions are welcome! If you have ideas for improvements or bug fixes, please fork the repository and submit a pull request. Remember to remove or secure any sensitive information in your contributions.

License

This project is licensed under the MIT License. See the LICENSE file for more details.

Disclaimer

This tool is provided as-is. Ensure you secure your API keys and credentials. Use responsibly, especially when handling personal or sensitive data.

⸻

Happy coding and fitness tracking!
