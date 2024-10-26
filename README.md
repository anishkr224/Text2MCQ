# Automated MCQ Generation System Using NLP

**Project Overview**: Developed an automated MCQ (Multiple Choice Question) generator that leverages Natural Language Processing (NLP) techniques to parse text input, extract key entities, and create contextually relevant question-answer choices.

Implemented **natural language processing (NLP)** techniques with **SpaCy** for advanced text parsing, noun extraction, and random sampling to generate contextually relevant MCQs with multiple-choice options.

**Enhanced efficiency** by integrating the **PyPDF2** library for PDF text extraction and automated question generation, reducing manual input requirements by over **80%**.

**Validated user interactions** with a scoring system and feedback logic in JavaScript, achieving a fully functional interactive quiz interface with real-time feedback.

**Technical Skills Applied**: Python, NLP (spaCy), PyPDF2, Flask, Bootstrap, HTML/CSS/JS.

### Here’s a breakdown of its structure and functionality:

1. **Dependencies**: 
   - `spacy` for NLP tasks, specifically to parse text and identify nouns.
   - `PyPDF2` to handle PDF text extraction.
   - `Flask` for the web framework and `flask_bootstrap` for UI styling.
   
2. **NLP-based MCQ Generation**:
   - The `generate_mcqs` function processes input text to create MCQs. It identifies sentences, extracts nouns, and uses the most common noun in each sentence as the answer choice, while adding distractors.
   - This function ensures there are enough nouns to create multiple choices and that a minimum of four answer choices is available by adding placeholders if needed.

3. **File Handling**:
   - The `process_pdf` function reads PDFs using `PdfReader` from `PyPDF2`. It extracts and aggregates text across all pages.

4. **Web Interface**:
   - The `index` route accepts manual text input or file uploads (PDF or text) and processes them to create MCQs.
   - If no valid MCQs are generated, the user is prompted to try different input.

5. **User Input and Feedback**:
   - The application lets users choose the number of questions, with error handling for insufficient text or unsupported formats.

To deploy this, ensure you have the required dependencies in your environment (`Flask`, `Flask-Bootstrap`, `spacy`, `PyPDF2`) and install the `en_core_web_sm` model in spaCy.

### Result: Below are the resulting videos.

![Result video](./Output/Output.gif)

### Result: 

    https://youtu.be/CHrirxy6-FA?si=RL8NqZJrlI6KCW1B


