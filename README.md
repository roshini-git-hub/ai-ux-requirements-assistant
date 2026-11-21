# AI-Powered UX Requirements Assistant

An NLP-powered application that transforms natural-language product ideas into structured UX requirements, design recommendations, and technology-specific development prompts.

## Overview

Planning a website or mobile application requires understanding its users, goals, features, pages, and design requirements.

This project simplifies that process through an interactive AI-assisted requirements interview.

Users describe their application idea in natural language. The system analyzes the input, asks relevant follow-up questions, identifies the application domain, recommends pages and features, retrieves relevant UX guidelines, and generates structured project documentation.

## Key Features

- **Natural Language Processing:** Extracts product requirements from user descriptions.
- **Domain Classification:** Identifies application domains such as food ordering, e-commerce, education, healthcare, and banking.
- **Interactive Requirements Interview:** Asks follow-up questions to collect missing requirements.
- **Page Recommendations:** Suggests relevant application pages based on the selected domain and requirements.
- **Feature Recommendations:** Recommends features from predefined domain knowledge.
- **Semantic UX Retrieval:** Retrieves relevant UX guidelines using sentence embeddings and cosine similarity.
- **Design Recommendations:** Generates visual design direction, color palettes, and UX suggestions.
- **Development Prompt Generation:** Creates technology-specific development prompts.
- **Report Generation:** Produces detailed project reports in Markdown and DOCX formats.
- **Session Management:** Supports saving and resuming project interviews.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core implementation |
| spaCy | Natural language processing |
| Sentence Transformers | Text embeddings |
| all-MiniLM-L6-v2 | Semantic representation of text |
| scikit-learn | Cosine similarity |
| NumPy | Numerical operations |
| Gradio | Interactive user interface |

## Supported Application Domains

- Food Ordering
- E-commerce
- Education
- Healthcare
- Banking

## Supported Development Stacks

The project includes development prompt templates for:

- React + Vite + TypeScript + Tailwind CSS
- Next.js + TypeScript + Tailwind CSS
- React Native + Expo + TypeScript
- Flutter
- HTML + CSS + Vanilla JavaScript

## How It Works

1. **User Input:** The user describes the website or application they want to build.
2. **Requirement Extraction:** The system identifies relevant information from the natural-language description.
3. **Domain Classification:** Semantic similarity and keyword matching help identify the application domain.
4. **Interactive Interview:** The system asks questions to collect missing requirements.
5. **UX Recommendations:** The system recommends pages, features, design direction, and UX guidelines.
6. **Semantic Retrieval:** Relevant guidelines are retrieved from the predefined UX knowledge base.
7. **Report Generation:** The collected requirements are converted into a structured report.
8. **Development Prompts:** Technology-specific prompts are generated from the project requirements.

## Installation

Install the required dependencies:

```bash
pip install spacy sentence-transformers gradio scikit-learn numpy
python -m spacy download en_core_web_sm
```

## Running the Project

1. Open `nlp.ipynb` in Google Colab or Jupyter Notebook.
2. Run the notebook cells in order.
3. Wait for the required models and dependencies to load.
4. Launch the Gradio application using the final application cell.
5. Open the generated Gradio interface and describe your application idea.

## Example Input

```text
I want to build a food delivery app for college students.
It should support online payments and have a playful design.
```

## Example Output

The system can collect requirements such as:

- Application domain: Food Ordering
- Target users: College Students
- Platform: Mobile
- Authentication: Required
- Payment: Required
- Visual style: Playful

It can then recommend relevant pages, features, UX guidelines, and development prompts based on the collected requirements.

## Project Structure

```text
ai-ux-requirements-assistant/
│
├── nlp.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
└── screenshots/
    └── demo.png
```

## Current Scope and Limitations

- Domain knowledge and UX guidelines are maintained in predefined knowledge bases.
- Requirement extraction uses implemented NLP and matching logic.
- Semantic retrieval depends on the available knowledge base.
- Development prompts are generated from templates and collected project requirements.
- The project generates requirements, reports, and prompts; it does not automatically deploy a finished application.

## Future Improvements

- Expand the domain knowledge base.
- Improve requirement extraction for complex user descriptions.
- Integrate an LLM for more flexible conversational understanding.
- Add persistent cloud-based project storage.
- Add a visual interface for reviewing generated UX recommendations.
- Evaluate domain classification and retrieval quality using a larger test dataset.
