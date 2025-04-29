# Weather_daily_report
This project creates an automated daily weather report for Austin TX using open-source data. Here are the steps:

## A. Sign up for Open Weather
1. Sign up for an account: Register on [OpenWeatherMap](https://openweathermap.org/) to access the API.
2. Generate an API key: Create a new API key in the account dashboard.
3. Explore the API documentation: Review the Current Weather [Data guide](https://openweathermap.org/current) to understand request parameters and responses.
4. Test the API in Postman: Send a request in Postman to retrieve real-time weather data for your city.

## Visualize weather data
The Open Weather Map data is visualized in a notebook (weather_data.ipynb) using Matplotlib library. The Pandas dataframe is savaed locally.

## Email API
1. A new notebook (email_API.ipynb) is created to first test email functionality.
2. There are 2 ways to programmatically send emails via Python:  
   i) Simple SMTP method similar to [this](https://stackabuse.com/how-to-send-emails-with-gmail-using-python/).  
   ii) Professional services like Sendgrid, using their API. We choose this method.
3. Sign Up for a free SendGrid account. Create a Sender Profile and Send the first email following [this guide](https://app.sendgrid.com/guide/integrate).
4. 'pip install sendgrid'
5. We verify the email sent via the API is delivered to our mailbox.

## Send weather report through email
1. A new notebook (send_weather_report_email.ipynb) is created that combines the previous 2 notebooks.
2. This notebook formats the weather data and graphics into a clean HTML template, and automatically emails you the compiled weather report when executed.

## Using AWS to automate daily emails
1. An AWS Lambda Function is created and the code from the combining notebook is copied into it.
2. A Cloudwatch schedule is created to send emails daily.

