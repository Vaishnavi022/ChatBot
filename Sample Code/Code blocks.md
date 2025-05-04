# Electronics Troubleshooting Chatbot: Streamlit + Gemini Integration

This chatbot allows users to describe an issue or upload an image for analysis. The backend utilizes Google's Gemini API to process the request and diagnose issues in electronics.

## Block 1: Import Libraries and Load Environment Variables

```python
from dotenv import load_dotenv
load_dotenv()  # Load environment variables from .env.

import streamlit as st
import os
import textwrap
import google.generativeai as genai
from PIL import Image


# Explanation:
# dotenv is used to load environment variables (like your API key) from a .env file.
# Streamlit provides an easy way to create the web interface for the chatbot.
# os helps interact with the operating system, like fetching the API key.
# textwrap is used to format the generated text neatly.
# google.generativeai is the Gemini API used to generate content and analyze text and images.
# PIL (Python Imaging Library) is used to handle image uploads.
