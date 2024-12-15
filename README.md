AI Medication Schedule Generator

This project demonstrates a Python-based application that generates a medication schedule using speech input, processes the data with Google's Generative AI, and sends the schedule as a PDF via email. It uses various libraries and tools to achieve this functionality.

Features:
  Speech-to-Text Conversion - Converts audio input to text using the SpeechRecognition library and the Google Web Speech API.
  AI-Powered Data Generation - Processes the converted text with Google's Generative AI (Gemini-1.5-flash model) to create structured medication details.
  JSON to Table Conversion - Converts AI-generated JSON output into a readable tabular format.
  PDF Generation - Creates a PDF of the medication schedule using the FPDF library.
  Email Integration - Sends the generated PDF to a specified recipient via email.

Prerequisites
1. Python Version - Python 3.8
   
2. Required Libraries - Install the following libraries:
  pip install google-generativeai==0.3.0
  pip install SpeechRecognition==3.8.1
  pip install pydub==0.25.1
  pip install fpdf==1.7.2

3. Google API Key - Obtain a Google API key for using Google's Generative AI.Replace the placeholder in the configure_model function with your API key.

How to Use
1. Prepare Audio Input
Ensure your audio file is in a supported format (e.g., .wav, .mp3).
3. Workflow
Upload an audio file.
The script converts the audio to text.
The text is processed using Google's Generative AI.
A structured medication schedule is generated and saved as a PDF.
The PDF is sent to the recipient's email.

Configuration Details

1. Email Setup
Replace sender_email and password in the send_email_with_pdf function with your email credentials.
Note: For Gmail, you need to use an App Password, which can be created from your Google Account settings.

2. API Configuration
Replace the placeholder in the configure_model function with your actual Google API key.

File Structure
main.py: The primary script containing all functions.
temp.wav: Temporary WAV file generated during the speech-to-text process.
medication_schedule.pdf: PDF file generated with the medication schedule.

Libraries and Tools Used
google-generativeai - For integrating with Google's Generative AI.
SpeechRecognition - For converting speech input to text.
pydub - For audio file format conversion and processing.
fpdf - For generating PDFs.
smtplib - For sending emails with attachments.

Troubleshooting
SpeechRecognition Errors:Ensure proper audio file format.Check network connection for accessing Google Web Speech API.
AI Response Errors:Verify the API key and configuration.
PDF Generation Issues:Ensure Unicode compatibility for special characters.
Email Sending Errors:Ensure the sender email is configured correctly.Use App Passwords for Gmail.
