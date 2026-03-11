# DHC-ML-Task_4
Health Assistant Chatbot - A Python-based AI Health Assistant using the Llama-3.1-8B-Instruct model to provide general medical information.

## Task Objective
The goal of this project is to develop an automated Health Assistant that provides general health information using an LLM while ensuring user safety. It implements a custom safety filter to block queries regarding medication dosages and specific medical treatments.

## Dataset & Model Used
- **Model:** `meta-llama/Llama-3.1-8B-Instruct` (via Hugging Face Inference API).
- **Data:** This project uses real-time user queries and a predefined list of unsafe keywords for safety filtering.
- **Libraries:** `requests`, `json`, `matplotlib`.

## Models Applied
- **LLM:** Llama-3.1-8B for natural language understanding and response generation.
- **Safety Logic:** A rule-based keyword matching system combined with specialized System Prompting.

## Key Results and Findings
- **Successful API Integration:** The system successfully communicates with the Hugging Face Inference Router.
- **Safety Enforcement:** High-risk keywords like 'dosage', 'tablets', and 'prescription' are effectively intercepted by the `is_unsafe` function before reaching the LLM.
- **Prompt Engineering:** The use of a structured System Prompt ensures the LLM provides responses in a consistent format (Possible Causes, Prevention Tips, When to See a Doctor).
- **Future Improvements:** Transitioning from keyword matching to a semantic-based safety model (like BERT) would improve the robustness of the filter.
