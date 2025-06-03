This project is a Q&A chatbot that extracts and answers questions about invoice images using Google’s Gemini 1.5 Flash model and a clean Streamlit frontend.

🌟 Features
Upload invoice images in .jpg, .jpeg, or .png format

Ask questions like “What is the invoice number?”, “What is the total amount?”

Uses Google’s Gemini model to interpret and extract details from invoices

Simple and interactive web interface built with Streamlit

Displays both the uploaded image and the response

🛠 Technologies Used
Python – Backend logic

Streamlit – Web interface

Google Generative AI – Image understanding (Gemini 1.5 Flash)

PIL (Python Imaging Library) – Image processing and display

dotenv – Securely manage API keys

🧠 How It Works
The user uploads an image of an invoice.

The user types a question such as:

“What is the invoice date?”

“What items were purchased?”

“How much GST is charged?”

The app sends:

A system prompt that explains to the model that it is reading an invoice.

The image in byte format.

The user’s question.

Gemini analyzes the image and question, and returns a human-readable response.

The app displays the answer below the image.

🗂 Code Overview
Environment Setup

API key is loaded using dotenv for secure configuration.

Gemini Response Function

Accepts a question, image, and system prompt, and calls Gemini 1.5 Flash.

Image Preprocessing

Uploaded image is converted to byte format with MIME type.

Streamlit UI

Provides input prompt, file uploader, and displays the image and model response.

Prompt Template

A fixed instruction telling Gemini that the image will be an invoice and it must answer questions based on it.

🎯 Use Case Examples
Automate data entry from scanned invoices

Perform audits on invoices by querying specific fields

Extract line items, dates, totals, and tax information

Build backend logic for financial automation workflows

💡 Future Improvements
Add support for multi-page PDF invoices

Enable chat history for multiple Q&A rounds

Export structured data (like tables or JSON formats)

Improve invoice layout understanding with template-based OCR fallback

Add data validation rules for known invoice patterns

Allow users to download extracted data

