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

## Block 2: Format Output as Markdown
# Format Gemini output as Markdown
def to_markdown(text):
    text = text.replace('•', '  *')
    return textwrap.indent(text, '> ', predicate=lambda _: True)

#Explanation:
#This function converts the output from the Gemini model into a more readable Markdown format.
#It replaces bullet points with asterisks and indents the text for better presentation in Streamlit.


## Block 3: Configure Gemini API and Analyze Function
# Configure Gemini API
genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))

# Combined analysis function (text + image)
def analyze_question_and_image(question, image=None):
    model = genai.GenerativeModel("models/gemini-1.5-flash-001")

    prompt = f"""
    You are an expert in electronics troubleshooting.

    I face the provided the following issue:
    \"{question}\"

    Analyze the image (if provided), identify any visible issues, and provide:
    1. A diagnosis based on the description and/or image.
    2. Explanation of the problem.
    3. Suggested fix or faulty component.
    """

    # Send both text and image to Gemini if image exists
    inputs = [prompt]
    if image:
        inputs.append(image)

    response = model.generate_content(inputs)
    return response.text

#Explanation:
#The Gemini API is configured using the API key loaded from the .env file.
#The analyze_question_and_image function sends a prompt to the Gemini model, which uses both the textual description and any uploaded image to generate an analysis.
#The function returns a detailed diagnosis and suggestions for the issue.

#Block 4: Streamlit UI and Interaction
# Streamlit UI
st.set_page_config(page_title="Electronics Troubleshooting Chatbot")
st.header("🔧 Conversational Image Chatbot")

# User Inputs
txt_input = st.text_input("Describe the issue or ask a question:", key="input")
uploaded_image = st.file_uploader("Upload an image (optional)", type=["png", "jpg", "jpeg"])

# Display uploaded image if any
if uploaded_image:
    st.image(uploaded_image, caption="Uploaded Image")  # Fixed: no use_container_width
    image = Image.open(uploaded_image)
else:
    image = None

# Unified submit button
submit_all = st.button("Analyze & Answer")

# Handle button click
if submit_all:
    if not txt_input and not uploaded_image:
        st.warning("Please enter a question or upload an image!")
    else:
        st.subheader("Diagnosis & Solution:")
        response = analyze_question_and_image(txt_input, image)
        st.write(response)

#Explanation:
#Streamlit UI setup: This block configures the page title and header, followed by input fields for the user to enter a question or upload an image.
#Image Upload: If the user uploads an image, it is displayed on the UI and passed for analysis.
#Analysis Button: The "Analyze & Answer" button triggers the analysis and displays the result. If no input is provided, a warning is shown to the user.
