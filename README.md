# JobSage: AI Mock Interview Coach (Google GenAI Capstone Project - 2025Q1)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This repository contains the Kaggle Notebook submission for the **Google Generative AI Intensive Course Capstone (March/April 2025)**.

**Project Goal:** To develop JobSage, an AI-powered mock interview simulator designed to provide more insightful, personalized, and actionable feedback than traditional practice methods, specifically targeting technical roles (e.g., Data Science at FAANG).

## Notebook:

*   **[`JobSage_Capstone_Submission.ipynb`](./jobsage kaggle submission.ipynb)**: The primary submission file. This notebook implements the core JobSage logic and demonstrates its functionality.

## Key Features Implemented (in Notebook):

*   **AI-Driven Mock Interview:** Simulates a multi-question interview session.
*   **Adaptive Difficulty:** Adjusts question difficulty based on user performance.
*   **Granular Feedback:** Uses the Gemini API to evaluate answers on Content, Clarity, and Depth, providing scores and qualitative feedback.
*   **Dynamic Follow-ups:** Generates context-aware follow-up questions using the Gemini API.
*   **Skill Tracking:** Identifies relevant skills per question and tracks performance (based on similarity scores).
*   **Gamification:** Includes points per question (scaled by difficulty), end-of-session badges, and leaderboard context.
*   **Benchmarking:** Compares user performance score against simulated FAANG norms.
*   **RAG for Recommendations:**
    *   **Jobs:** Recommends jobs from a static list based on semantic similarity between user CV embedding and job description embeddings.
    *   **Study:** Recommends study topics based on identified weak skill areas by retrieving relevant advice.
*   **Resume Tweak Suggestions:** Uses the Gemini API to suggest CV improvements based on weak skills identified during the interview.
*   **Negotiation Simulator:** Uses the Gemini API to generate a simulated salary negotiation dialogue and feedback based on user inputs.
*   **Interactive Demo:** Includes an optional Gradio interface embedded within the notebook for interacting with the core interview cycle and negotiation simulator.

## GenAI Capabilities Demonstrated:

*   **Embeddings:** Sentence Transformers (`all-MiniLM-L6-v2`) for semantic similarity scoring and RAG retrieval.
*   **Few-Shot Prompting:** Demonstrated with Gemini API for candidate question generation.
*   **Retrieval Augmented Generation (RAG):** Vector similarity search for job recommendations; Context-based retrieval for study tips.
*   **Structured Output / Controlled Generation / GenAI Evaluation:** Using Gemini API for multi-dimensional scoring, formatted feedback, skill extraction (JSON), follow-up question generation, and negotiation simulation/feedback.

## Technologies Used (in Notebook):

*   Python 3
*   Google Gemini API (`google-generativeai`)
*   Sentence Transformers (`sentence-transformers`)
*   Pandas, NumPy, SciPy
*   Gradio (for optional demo)
*   Kaggle Notebooks Environment

## Running the Notebook:

1.  Open the `.ipynb` file in Kaggle, Google Colab, or a local Jupyter environment.
2.  Ensure you have the required libraries installed (see `!pip install` command in the first code cell).
3.  Add your `GEMINI_API_KEY` as a Kaggle Secret (or environment variable if running locally).
4.  Run the cells sequentially from top to bottom.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
