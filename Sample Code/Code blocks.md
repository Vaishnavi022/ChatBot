## Block 1: Import Libraries and Load Environment Variables

```python
from dotenv import load_dotenv
load_dotenv()  # Load environment variables from .env.

import streamlit as st
import os
import textwrap
import google.generativeai as genai
from PIL import Image


## Explanation:
# dotenv: This library is used to load environment variables from a .env file, such as your API key, which ensures sensitive data is not exposed in your code.
# streamlit: A framework used to create the web interface for the chatbot. It makes it easy to build interactive applications with Python.
# os: A module that helps you interact with the operating system. In this case, it's used to fetch environment variables (like the API key for Gemini).
# textwrap: A utility to format long text for better readability. It is especially useful for wrapping text or creating indented sections.
# google.generativeai: This is the Gemini API, which provides the underlying generative AI model used to analyze the text and images submitted by users.
# PIL (Python Imaging Library): A powerful library for handling images in Python. In this case, it is used to handle image uploads and manipulate image data.

## How it Works
# load_dotenv(): This function loads the environment variables from the .env file. It's typically used to keep sensitive information (like your API key) separate from the 
  main codebase.
# genai.configure(api_key=os.getenv("GOOGLE_API_KEY")): This line configures the Gemini API client with the API key loaded from the environment variables, allowing the 
  chatbot to use Gemini for content generation and image analysis.

## Dependencies
# python-dotenv: Required to load environment variables from a .env file.
# streamlit: The framework used for building the UI.
# google-generativeai: Required for interacting with the Gemini API.
# Pillow: Python Imaging Library (PIL) for image processing.

 
