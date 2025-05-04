# Block 2: Formatting Gemini Output as Markdown

This block defines a helper function to format the **Gemini model's output** into **Markdown**. This makes the chatbot responses more readable and visually structured when displayed in the Streamlit app.

## Code

```python
# Format Gemini output as Markdown
def to_markdown(text):
    text = text.replace('•', '  *')
    return textwrap.indent(text, '> ', predicate=lambda _: True)

```
## Explanation:
to_markdown(): A helper function designed to format the text output from the Gemini model into Markdown syntax, so it displays neatly in the Streamlit interface.
replace('•', ' *'): This line replaces bullet points (•) from the raw Gemini output with Markdown-compatible list bullets (*). This allows the list items to render correctly in Markdown format.
textwrap.indent(): This indents each line of the text using the > symbol, turning it into a blockquote in Markdown. This gives the output a clean, indented look in the Streamlit app.

## How It Works:
The function receives the raw text output from Gemini.
It replaces bullet points (•) with the Markdown bullet symbol (*).
It then indents every line with > to convert the text into a blockquote, which is a common Markdown formatting style for displaying responses or quotes.
Finally, the formatted text is returned and rendered in the Streamlit app with proper Markdown formatting.

## Why This is Useful:
Makes the chatbot responses readable and clean.
Ensures lists and points from Gemini display properly as bullet points.
Uses Markdown blockquotes to visually differentiate model responses from user inputs or other content in the UI.

